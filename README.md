# RealTimeTranslator



[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1jTHQZxrdfzsDUyHHBTFKdw6k7f9we7Dt#scrollTo=VgVsFPp7P6rt)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Gradio Interface](https://img.shields.io/badge/Interface-Gradio-FF4B4B?style=for-the-badge)]
![Whisper](https://img.shields.io/badge/ASR-Whisper-000000?style=for-the-badge)

Мощная система для перевода речи в реальном времени с сохранением характеристик голоса. Поддерживает множество языков и обеспечивает высокое качество синтеза.

![RealTime Translator Interface](https://drive.google.com/uc?export=view&id=1xWSWulLBXspWvcAIYtg60I80uTYrI4M5)
![RealTime Translator Interface](https://drive.google.com/file/d/1QdSTx_uVj7uUQc1rP3yppKde2Jco9QpD/view?usp=drive_link)
![RealTime Translator Interface](https://drive.google.com/file/d/1u7uukCgPvSy0MmJ72YRfxi5bZMU7i48d/view?usp=drive_link)

## ✨ Возможности

- **🎤 Распознавание речи** - Автоматическое определение языка с помощью Whisper Medium
- **🌍 Мультиязычный перевод** - Поддержка 9+ языков через Google Translate API
- **🎵 Сохранение голоса** - Анализ и применение характеристик голоса (pitch, tempo, energy)
- **⚡ Real-time обработка** - Быстрый отклик (<3 секунд)
- **🎨 Профессиональный интерфейс** - Интуитивный веб-интерфейс на Gradio

## 📋 Поддерживаемые языки

| Язык | Код | Статус |
|------|-----|--------|
| English | `en` | ✅ Полная поддержка |
| Russian | `ru` | ✅ Полная поддержка |
| German | `de` | ✅ Полная поддержка |
| French | `fr` | ✅ Полная поддержка |
| Spanish | `es` | ✅ Полная поддержка |
| Italian | `it` | ✅ Полная поддержка |
| Chinese | `zh` | ✅ Полная поддержка |
| Japanese | `ja` | ✅ Полная поддержка |
| Korean | `ko` | ✅ Полная поддержка |

## 🚀 Быстрый старт

### Запуск в Google Colab

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1jTHQZxrdfzsDUyHHBTFKdw6k7f9we7Dt#scrollTo=VgVsFPp7P6rt)

1. Откройте ноутбук в Google Colab по ссылке выше
2. Выполните все ячейки по порядку
3. Дождитесь запуска веб-интерфейса
4. Начните использовать переводчик!


## 📦 Зависимости

Основные зависимости:
- `torch` & `torchaudio` - ML фреймворк
- `openai-whisper` - Распознавание речи
- `gTTS` - Синтез речи
- `gradio` - Веб-интерфейс
- `librosa` - Анализ аудио
- `deep-translator` - Перевод текста


## 🎮 Использование

### Через веб-интерфейс

1. **Загрузка аудио**: Используйте микрофон или загрузите аудиофайл
2. **Выбор языка**: Укажите целевой язык перевода
3. **Обработка**: Нажмите "Начать перевод"
4. **Результат**: Получите текст и синтезированную речь

### Программный API

```python
from translator import AdvancedSpeechTranslator

# Инициализация
translator = AdvancedSpeechTranslator()

# Обработка аудио
text, audio, lang = translator.process_audio_translation(
    "path/to/audio.wav", 
    target_lang="fr"
)
```

## 🏗️ Архитектура системы

```
Input Audio → Whisper ASR → Text → Google Translate → 
Translated Text → gTTS → Voice Processing → Output Audio
```

### Компоненты:

1. **ASR Module** - Whisper Medium для распознавания
2. **Translation Engine** - Google Translate API
3. **TTS Module** - gTTS с мультиязычной поддержкой
4. **Voice Processor** - Анализ pitch/tempo/energy
5. **Web Interface** - Gradio для взаимодействия

## ⚙️ Настройка

### Конфигурационные параметры

```python
# Настройки модели
WHISPER_MODEL = "medium"  # base, small, medium, large
TTS_ENGINE = "gTTS"       # Google Text-to-Speech
SUPPORTED_LANGUAGES = ["en", "ru", "de", "fr", "es", "it", "zh", "ja", "ko"]
```

### Переменные окружения

```bash
export GOOGLE_TRANSLATE_KEY="your_api_key"
export WHISPER_CACHE_DIR="./models"
```

## 📊 Производительность

- **Время обработки**: < 3 секунд
- **Точность распознавания**: > 90%
- **Поддержка языков**: 9+
- **Качество синтеза**: Высокое (естественное звучание)

## 🤝 Contributing

Мы приветствуем вклад в проект! 

1. Форкните репозиторий
2. Создайте feature branch
3. Commit ваши изменения
4. Push в branch
5. Создайте Pull Request

## 📝 Лицензия

Этот проект распространяется под лицензией MIT. См. файл `LICENSE` для подробностей.

## 🆘 Поддержка

Если у вас возникли проблемы:

1. Проверьте [Issues](https://github.com/yourusername/realtime-translator/issues)
2. Создайте новое issue с описанием проблемы
3. Укажите версии библиотек и ошибки

## 🔮 Планы развития

- [ ] Поддержка большего количества языков
- [ ] Улучшение качества сохранения голоса
- [ ] API для разработчиков
- [ ] Мобильное приложение
- [ ] Оффлайн-режим

---

**⭐ Если проект вам понравился, не забудьте поставить звезду на GitHub!**

[Open in Colab](https://colab.research.google.com/drive/1jTHQZxrdfzsDUyHHBTFKdw6k7f9we7Dt#scrollTo=VgVsFPp7P6rt) | [GitHub Repository](https://github.com/yourusername/realtime-translator)




## 📞 Контакты

**💬 По вопросам сотрудничества и предложениям:**

<div align="center">

### 📧 Электронная почта
[![Email](https://img.shields.io/badge/📩-AlinaSGrib@gmail.com-8B89CC?style=for-the-badge&logo=gmail&logoColor=white)](mailto:AlinaSGrib@gmail.com)

### 💻 GitHub
[![GitHub](https://img.shields.io/badge/🐙-Alino4kaAlino4ka-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Alino4kaAlino4ka)

### 📱 Telegram
[![Telegram](https://img.shields.io/badge/✈️-@Alino4kaGribavova-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/Alino4kaGribavova)

</div>

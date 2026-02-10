Этот репозиторий содержит последнюю и актуальную версию книги, находящуюся в процессе написания

Книга достаточно объемна и планируется к окончанию в феврале 2027 года, при текущем темпе написания 
глав и подготовки материалов. 

Книга первой версии, поэтому учитывайте это, когда будете видеть ошибки и опечатки, 
по которым крайне буду рад, если вы мне напишите на следующие контакты:

    readthis@inbox.ru
    @xPushNotification

# Оглавление

1. Интро
2. [Введение](ax001-introduction.md)

## Вводный раздел:

1. [Вводим принципы разработки](ax002-selected-development-principles.md)
2. [Выбираем архитектуру для разработки](ax003-selected-architecture.md)
3. [Выбираем модель для авторизации](ax004-selected-auth-model.md)

# Софт скилз

1. [Тактический аджайл для разработчиков](ax005-tactical-agile.md)
2. [Управление хаосом в разработке (давление неизвестности)](ax006-managing-chaos.md)
3. [Эффективность разработчика (давление перфекционизма)](ax007-efficiency-principles.md)

# Концептуальный раздел

1. Пред-спринг приложение с помощью инверсии контроля
2. Перенос пред-спринг прототипа на Spring framework
3. Развертывание обеспечивающей инфраструктуры
    - kafka
    - rabbit mq
    - базы данных
    - redis
    - zipkin
    - docker (нам хватит встроенного kubernetes)
    - проверки на работающую инфраструктуру через отдельную инфраструктурную микру
4. TDD и BDD как принципиальный элемент разработки
5. Git (trunk-based/release-flow стратегии)
6. Jira и аналоги для контроля флоу задач
7. Бизнес и архитектурные концепции
    - логические компоненты
    - кодовые абстракции
8. Транзакции как фундаментальный элемент проектирования
9. Бухгалтерский модуль как основа финансового процессинга
10. Смарт контракты и их аналоги на спринге

# Базовый каркас Spring и конфигурации

1. Выбранные микросервисы для демонстрации и их логика
2. История про properties и profiles
3. Кастомное создание бинов и предпроцессоры
4. Работа с контекстом напрямую
5. Стартеры и автоконфигурация
6. Создание кастомных стартеров
7. Модульная архитектура на базе Maven и Gradle
8. Работа с classpath для подключений объектов программы
9. Секреты (Vault и Jasypt)
10. Работа со SpEL
    - скриптование в аннотациях
    - скриптование из внешних источников (задание правил) + изолирование в песочнице
11. Жизненный цикл (ApplicationListener, CommandLineRunner)
12. JavaDoc

## Тестирование и рефакторинг

1. Тесты в отдельном модуле
2. Профилирование по скорости
3. Стратегии оформления модулей
4. Вывод кода в "отставку"
5. Итерационная разработка
6. Кукумбер для сценариев бизнес логики
7. Юнит тесты (JUnit, Mockito)
8. Слои тестирования (репозиторий, веб-слой и так далее)
9. Эмуляция работы пользователя (действия из под профиля)
10. Интеграционные тесты и стратегия очистки после перезапуска

## Данные и персистентность

1. Spring Data JPA (Hibernate)
2. JDBC & JdbcTemplate
3. Хранимые процедуры (JPA/JdbcTemplate)
4. Criteria API
5. Транзакции (разные транзакционные менеджеры) + default-методы
6. Миграции БД (Liquibase)
7. H2 + PostgresSQL совместимость
8. Spring Data MongoDB
9. Spring Data Redis
10. Avro схемы для получения сериализируемых байтовых представлений для пересылок

# Бизнес логика и управление состоянием

1. Публичный id (IK/IC) и внутрибазовый id и порядок работы с ними
2. Логин системного оператора и его роль в операциях
3. Notices для пользователей с отметкой о просмотре
4. Расширяемые объекты User против UserAddress 
5. Группирующие (связывающие) энтити 
   - по типу графов
   - по типу агрегаторов
   - использование feature флага
6. Логические очереди исполнения процессов и связывающие их энтити как корень 
7. Проектирование DTO как языка взаимодействия систем 
8. Загружаемые пользователем файлы и доступ к таким файлам
9. Загрузка и выгрузка данных в файлах
10. Принципы формирования и появления reports в системе (ad hoc, EOD, BOD и так далее) 
11. Sticky note для комментариев под энтити и добавление тегов классов
12. Параллельно работающие maintenance сервисы, шкедулинг таких сервисов
13. Spring State Machine как основа тестируемой бизнес логики
14. Саги через оркестрацию и хореографию
15. Spring Events асинхронные и синхронные
16. AOP (Aspect-Oriented Programming) как стратегия разработки
17. Spring Scheduler + ShedLock
18. Spring Batch : с джобами и задачами
19. Паттерн BFF (Backend For Frontend)
20. Camunda для бизнес процессов 
21. Кеширование
    - redis (именно для кеша, межсетевой)
    - кофеин (инмемори для одного процесса)
    - двухуровневка (сначала тест на локальное сохранение потом на редис потом пропогандирование)

## Безопасность

1. сертификат безопасности 
   - через Apache сервер и реверсивный прокси
   - через Spring напрямую
2. Keycloak и возможности управления и взаимодействия с ним
3. Spring Security Core 
4. Мульти-схема аутентификации
5. OAuth 2.0 (AS/RS/Client)
6. Fraud Control (фильтры - правила, списки, защиты)
7. Микросервис пользовательских данных
    - почему не используем Spring Session
    - хранение наборов ключей - если нужно
8. Кастомные аннотации безопасности
9. Обеспечение входа через Google авторизацию
10. Регистрация с активацией по имейлу
11. Безопасность на Kafka 
12. KMS (система управления ключами)
13. Логика 2FA (как часть MFA)
14. Стратегия хранения персональных данных и идентификации пользователей

## Веб уровень раздел

1. Rest API (Spring MVC, DTO, MapStruct)
2. resilience4j
    + load balancer (spring cloud load balancer)
    + circuit breaker
    + fallback
    + retry
    + bulkhead
3. Spring Data REST
4. OpenAPI 3 + SpringDoc + генерация клиентов
5. Глобальные обработчики исключений
6. Валидация + кастомные валидаторы
7. WebClient (таймауты, retry, fallback)
8. Веб-сокеты (STOMP) 
9. Высокоскоростное сокетное соединение
10. GraphQL
11. Spring cloud function

## Реактивные и event-driven системы

1. Project Reactor
2. Spring WebFlux
3. R2DBC
4. Reactive Security
5. Message Brokers (Kafka, RabbitMQ, Spring Cloud Stream
    - эволюция от самописного аналога Kafka до промышленной системы
6. Transactional Outbox
7. CQRS + Event Sourcing

## Распределенные системы раздел

1. Service Discovery (Eureka)
2. API Gateway + кэшер BFF + Spring Cloud Balancer
3. Feign Client
4. Распределенная конфигурация (конфиг сервер)
5. ELK-стек
6. Наблюдаемость (метрики, трассировка) через Spring Cloud Sleuth / Actuator / Graphana etc.
   Micrometer Tracing and Zipkin, сценарии использования метрик:
   - System Performance Metrics
   - Queries Per Second (QPS)
   - Measures incoming requests per second
   - Transactions Per Second (TPS)
   - Measures completed transactions per second
   - Concurrency
   - Tracks simultaneous active requests
   - Response Time (RT)
   - Measured from request start to response received.
7. ClickHouse
8. Кэширование в распределенных системах (Spring Cache + Redis)
9. Hadoop

## Сборка и развертывание

1. Docker & Docker Compose
2. Kubernetes + клиент спринга для кубера
3. Load balancing (в гейтвее и в кубернетис)
4. CI/CD (Jenkins pipeline)
5. Версионирование API
6. Версионирование схем данных 
7. Disaster recovery

## Приложения:

1. ДДД (пример с ивент сорсингом, агрегаторами и тд.) и его проблемы
2. Хексагональная архитектура и её проблемы
3. Кредитный конвеер CRIF (CreditFlow, CreditAbility, CrifDelivery и так далее)
4. JOOQ, MyBatis
5. Debezium
6. Quarkus
7. OpenTelemetry/Jaeger
8. Hazelcast
9. Apache Solr
10. java rx
11. Terraform
12. Axon Framework
13. автотестирование
14. Spring Cloud Stream
15. сервисный меш Kiali
16. Running a blue-green deployment в кубере + канареечные релизы + feature flags
17. kafka connect - конвееризация данных через кафку (передача данных между инфраструктурой)
18. vulnerability scanning tools
19. код форматировщики и станданртировщики опять же для кода (из башки)
20. Chaos Engineering (Gremlin, Chaos Monkey) - для тестирований
21. Микросервисные паттерны
    - Service discovery
    - Edge server
    - Reactive microservices
    - Central configuration
    - Centralized log analysis
    - Distributed tracing
    - Circuit breaker
    - Control loop
    - Centralized monitoring and alarms
    - так далее

© 2026 Vladimir Nizov. All rights reserved. See the COPYRIGHT file for details.

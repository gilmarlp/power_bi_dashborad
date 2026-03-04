# Power BI Dashboards

Dashboard do setor de RH de uma empresa, com indicadores de número de funcionários, indicadores de desempenho, engajamento, satisfação e equilíbrio de vida pessoal e trabalho, com filtro de condição na empresa.

## Expressões DAX utilizadas para criação de novas colunas

- `IsActive = IF('employee_data'[EmployeeStatus] = "Active", 1, 0)`

- `TenureYears =
  VAR EndDate =
      IF(
          ISBLANK('employee_data'[ExitDate]),
          TODAY(),
          'employee_data'[ExitDate]
      )
  RETURN
  DATEDIFF('employee_data'[StartDate], EndDate, YEAR)`

- `Age = DATEDIFF('employee_data'[Birth Date], TODAY(), YEAR)`

## Exemplo da tabela após limpeza e formatação dos dados e criação de novas colunas com informações importantes
<img width="1920" height="1032" alt="Captura de tela 2026-02-18 150448" src="https://github.com/user-attachments/assets/b7561659-7b49-465f-a2c0-8b01a10d26ce" />

## Sem filtros aplicados
<img width="1447" height="818" alt="Captura de tela 2026-02-19 144213" src="https://github.com/user-attachments/assets/9a9f6984-eb2c-4d4e-b23c-5710337c6651" />

## Com filtros aplicados
<img width="1440" height="810" alt="Captura de tela 2026-02-19 145149" src="https://github.com/user-attachments/assets/4db57b4a-e88b-48c4-b357-54f2d36b6f4d" />

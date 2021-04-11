---
description: Envia um trabalho para um sistema operacional para execução em uma data e hora especificadas no futuro.
ms.assetid: 9d582fbb-24cb-401d-8b77-af7671a24e6d
ms.tgt_platform: multiple
title: Método Create da classe Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9f1acae94ea29d2d57b2952c0b0adc267ad3066c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296119"
---
# <a name="create-method-of-the-win32_scheduledjob-class"></a>Método Create da classe Win32 \_ ScheduledJob

O método **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) envia um trabalho para um sistema operacional para execução em uma data e hora especificadas no futuro. Esse método requer que o serviço de agendamento seja iniciado no computador para o qual o trabalho é enviado.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Create(
  [in]           string   Command,
  [in]           datetime StartTime,
  [in, optional] boolean  RunRepeatedly,
  [in, optional] uint32   DaysOfWeek,
  [in, optional] uint32   DaysOfMonth,
  [in, optional] boolean  InteractWithDesktop,
  [out]          uint32   JobId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Comando* \[ no\]
</dt> <dd>

Nome do comando, programa em lotes ou arquivo binário e parâmetros de linha de comando que o serviço de agendamento usa para invocar o trabalho.

Exemplo: "Defrag/q/f".

</dd> <dt>

*StartTime* \[ no\]
</dt> <dd>

Tempo universal coordenado (UTC) para executar um trabalho. O formulário deve ser: "AAAAMMDDHHMMSS. MMMMMm (+-) OOO ", onde" aaaammdd "deve ser substituído por" \* \* \* \* \* \* \* \* ". Por exemplo: " \* \* \* \* \* \* \* \* 143000.000000-420" especifica 14,30 (2:30 P.M.) PST com o horário de verão em vigor.

A seção "(+-) OOO" do valor da Propriedade StartTime é a tendência atual para a conversão de hora local. A tendência é a diferença entre a hora UTC e a hora local. Para calcular a tendência de seu fuso horário, multiplique o número de horas em que o fuso horário está adiantado ou atrasado no horário de Greenwich (GMT) por 60 (use um número positivo para o número de horas se o fuso horário estiver à frente do GMT e um número negativo se o fuso horário estiver atrás do GMT). Adicione um 60 adicional ao seu cálculo se o seu fuso horário estiver usando o horário de verão. Por exemplo, o fuso horário padrão do Pacífico é de oito horas atrás do GMT, portanto, a tendência é igual a-420 (-8 \* 60 + 60) quando o horário de verão está em uso e-480 (-8 \* 60) quando o horário de verão não está em uso. Você também pode determinar o valor da tendência consultando a propriedade Bias da classe TimeZone do [**Win32 \_**](win32-timezone.md) .

</dd> <dt>

*RunRepeatedly* \[ em, opcional\]
</dt> <dd>

Se **for true**, um trabalho agendado será executado repetidamente em dias específicos. O padrão é **False**.

</dd> <dt>

*DaysOfWeek* \[ em, opcional\]
</dt> <dd>

Dias da semana em que um trabalho está agendado para ser executado; usado somente quando o parâmetro *RunRepeatedly* é **true**. Para agendar um trabalho para mais de um dia da semana, ingresse os valores apropriados em um OR lógico. Por exemplo, para agendar um trabalho para terças e sextas-feiras, o valor de *DaysOfWeek* é 2 ou 16.

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Segunda** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Terça-feira** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Quarta-feira** (4)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Quinta-feira** (8)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Sexta-feira** (16)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Sábado** (32)


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Domingo** (64)


</dt> <dd></dd> </dl> </dd> <dt>

*DaysOfMonth* \[ em, opcional\]
</dt> <dd>

Dias do mês em que um trabalho está agendado para ser executado; usado somente quando o parâmetro *RunRepeatedly* é **true**.

<dt>

<span id="1"></span>

<span id="1"></span>**1** (1)


</dt> <dd>

Dia 1 de um mês

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2** (2)


</dt> <dd>

Dia 2 de um mês

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3** (4)


</dt> <dd>

Dia 3 de um mês

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4** (8)


</dt> <dd>

Dia 4 de um mês

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5** (16)


</dt> <dd>

Dia 5 de um mês

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**6** (32)


</dt> <dd>

Dia 6 de um mês

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**7** (64)


</dt> <dd>

Dia 7 de um mês

</dd> <dt>

<span id="8"></span>

<span id="8"></span>**8** (128)


</dt> <dd>

Dia 8 de um mês

</dd> <dt>

<span id="9"></span>

<span id="9"></span>**9** (256)


</dt> <dd>

Dia 9 de um mês

</dd> <dt>

<span id="10"></span>

<span id="10"></span>**10** (512)


</dt> <dd>

Dia 10 de um mês

</dd> <dt>

<span id="11"></span>

<span id="11"></span>**11** (1024)


</dt> <dd>

Dia 11 de um mês

</dd> <dt>

<span id="12"></span>

<span id="12"></span>**12** (2048)


</dt> <dd>

Dia 12 de um mês

</dd> <dt>

<span id="13"></span>

<span id="13"></span>**13** (4096)


</dt> <dd>

Dia 13 de um mês

</dd> <dt>

<span id="14"></span>

<span id="14"></span>**14** (8192)


</dt> <dd>

Dia 14 de um mês

</dd> <dt>

<span id="15"></span>

<span id="15"></span>**15** (16384)


</dt> <dd>

Dia 15 de um mês

</dd> <dt>

<span id="16"></span>

<span id="16"></span>**16** (32768)


</dt> <dd>

Dia 16 de um mês

</dd> <dt>

<span id="17"></span>

<span id="17"></span>**17** (65536)


</dt> <dd>

Dia 17 de um mês

</dd> <dt>

<span id="18"></span>

<span id="18"></span>**18** (131072)


</dt> <dd>

Dia 18 de um mês

</dd> <dt>

<span id="19"></span>

<span id="19"></span>**19** (262144)


</dt> <dd>

Dia 19 de um mês

</dd> <dt>

<span id="20"></span>

<span id="20"></span>**20** (524288)


</dt> <dd>

Dia 20 de um mês

</dd> <dt>

<span id="21"></span>

<span id="21"></span>**21** (1048576)


</dt> <dd>

Dia 21 de um mês

</dd> <dt>

<span id="22"></span>

<span id="22"></span>**22** (2097152)


</dt> <dd>

Dia 22 de um mês

</dd> <dt>

<span id="23"></span>

<span id="23"></span>**23** (4194304)


</dt> <dd>

Dia 23 de um mês

</dd> <dt>

<span id="24"></span>

<span id="24"></span>**24** (8388608)


</dt> <dd>

Dia 24 de um mês

</dd> <dt>

<span id="25"></span>

<span id="25"></span>**25** (16777216)


</dt> <dd>

Dia 25 de um mês

</dd> <dt>

<span id="26"></span>

<span id="26"></span>**26** (33554432)


</dt> <dd>

Dia 26 de um mês

</dd> <dt>

<span id="27"></span>

<span id="27"></span>**27** (67108864)


</dt> <dd>

Dia 27 de um mês

</dd> <dt>

<span id="28"></span>

<span id="28"></span>**28** (134217728)


</dt> <dd>

Dia 28 de um mês

</dd> <dt>

<span id="29"></span>

<span id="29"></span>**29** (268435456)


</dt> <dd>

Dia 29 de um mês

</dd> <dt>

<span id="30"></span>

<span id="30"></span>**30** (536870912)


</dt> <dd>

Dia 30 de um mês

</dd> <dt>

<span id="31"></span>

<span id="31"></span>**31** (1073741824)


</dt> <dd>

Dia 31 de um mês

</dd> </dl> </dd> <dt>

*InteractWithDesktop* \[ em, opcional\]
</dt> <dd>

Se **for true**, o trabalho especificado deverá ser interativo, o que significa que um usuário pode fornecer entrada para um trabalho agendado enquanto o trabalho está em execução. O padrão é **False**.

</dd> <dt>

*JobID* \[ fora\]
</dt> <dd>

Número de identificador de um trabalho. Esse parâmetro é um identificador para um trabalho que está sendo agendado em um computador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de 0 (zero) quando bem-sucedido e um número diferente para indicar um erro. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Conclusão bem-sucedida**
</dt> <dd>

0

A solicitação é aceita.

</dd> <dt>

**Sem suporte**
</dt> <dd>

1

A solicitação não terá suporte.

</dd> <dt>

**Acesso negado**
</dt> <dd>

2

O usuário não tem o acesso necessário.

</dd> <dt>

**Falha desconhecida**
</dt> <dd>

8

Processo interativo.

</dd> <dt>

**demarcador não localizado**
</dt> <dd>

9

Não é possível encontrar o caminho do diretório para o arquivo executável do serviço.

</dd> <dt>

**Parâmetro inválido**
</dt> <dd>

21

Parâmetros inválidos foram passados para o serviço.

</dd> <dt>

**Serviço não iniciado**
</dt> <dd>

22

A conta em que esse serviço é executado é inválida ou não tem as permissões para executar o serviço.

</dd> <dt>

**Outras**
</dt> <dd>

23 4294967295

</dd> </dl>

## <a name="remarks"></a>Comentários

Se o trabalho agendado iniciar um programa interativo, como o bloco de notas, a propriedade **InteractWithDeskto** deverá ser definida como **true** ou a tela do programa não ficará visível. O processo ainda aparece no **Gerenciador de tarefas** , mesmo que ele não apareça na tela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_ScheduledJob Win32**](win32-scheduledjob.md)
</dt> </dl>

 


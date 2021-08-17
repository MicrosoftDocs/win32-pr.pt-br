---
description: A&de desanterioridade \# 32; O método de classe WMI tenta alterar a prioridade de execução do processo.
ms.assetid: ef012e9e-ff65-4881-835e-ddab23af9333
ms.tgt_platform: multiple
title: Método setanteriority da classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.SetPriority
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: decd5892d480e4f236ae9d7acdc1a25c018557166535c963eb35dc3f6f62ffa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675565"
---
# <a name="setpriority-method-of-the-win32_process-class"></a>Método setanteriority da \_ classe Process do Win32

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **setanteriority** tenta alterar a prioridade de execução do processo.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Prioridade* \[ do no\]
</dt> <dd>

Nova classe de prioridade para o processo. Observe que esses valores são diferentes daqueles explicitamente indicados na propriedade **Priority** do [**\_ processo Win32**](win32-process.md).

<dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Ocioso** (64)


</dt> <dd>

Especificado para um processo com threads que são executados somente quando o sistema está ocioso. Os threads do processo são admitidos pelos threads de um processo executado em uma classe de prioridade mais alta, por exemplo, uma proteção de tela. A classe de prioridade ociosa é herdada por processos filho.

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Abaixo do normal** (16384)


</dt> <dd>

Indica um processo que tem prioridade acima **da \_ \_ classe de prioridade ociosa**, mas abaixo da **\_ \_ classe de prioridade normal**.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)


</dt> <dd>

Especificado para um processo sem necessidade de agendamento especial.

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Acima do normal** (32768)


</dt> <dd>

Indica um processo que tem prioridade acima **da \_ \_ classe de prioridade normal**, mas abaixo da **\_ \_ classe de prioridade alta**.

</dd> <dt>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**Alta prioridade** (128)


</dt> <dd>

Especificado para um processo que executa tarefas de tempo crítico que devem ser executadas imediatamente. Os threads do processo capturam os threads de processos da classe de prioridade normal ou ociosa. Um exemplo é o Lista de Tarefas, que deve responder rapidamente quando chamado pelo usuário, independentemente da carga no sistema operacional. Use extrema atenção ao usar a classe de alta prioridade, porque um aplicativo de classe de alta prioridade pode usar quase todo o tempo de CPU disponível.

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Tempo real** (256)


</dt> <dd>

Especificado para um processo que tem a maior prioridade possível. Os threads do processo antecipam os threads de todos os outros processos, incluindo processos do sistema operacional que executam tarefas importantes. Por exemplo, um processo em tempo real que é executado por mais de um intervalo muito curto pode fazer com que os caches de disco não sejam liberados ou um mouse não responda.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Conclusão bem-sucedida** (0)
</dt> <dt>

**Acesso negado** (2)
</dt> <dt>

**Privilégio insuficiente** (3)
</dt> <dt>

**Falha desconhecida** (8)
</dt> <dt>

**Caminho não encontrado** (9)
</dt> <dt>

**Parâmetro inválido** (21)
</dt> <dt>

**Outro** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentários

para definir a prioridade em tempo real, o chamador deve ter o **SeIncreaseBasePriorityPrivilege** (**\_ \_ \_ \_ privilégio de prioridade BASE do ES INC**). Sem esse privilégio, a prioridade mais alta pode ser definida como prioridade alta.

## <a name="examples"></a>Exemplos

A amostra [Modificar a prioridade de um processo em execução](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) do VBScript altera a prioridade de uma instância em execução do Notepad.exe de normal para acima normal.

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

[**\_Processo Win32**](win32-process.md)
</dt> </dl>

 


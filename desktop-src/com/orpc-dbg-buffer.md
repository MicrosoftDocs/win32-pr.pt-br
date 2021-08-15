---
title: ORPC_DBG_BUFFER estrutura
description: A estrutura BUFFER DO DBG ORPC é o formato de buffer usado para marshalled de dados RPC para os métodos da \_ \_ interface IOrpcDebugNotify.
ms.assetid: 444cd3b8-bc7b-425d-9ccc-04fd6c7393b2
keywords:
- ORPC_DBG_BUFFER estrutura COM
- PORPC_DBG_BUFFER ponteiro de estrutura COM
topic_type:
- apiref
api_name:
- ORPC_DBG_BUFFER
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cb1f83cfcbe673cd2d5701e57ae1e94d4e04b59b845cd9ec7b617077da24bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310252"
---
# <a name="orpc_dbg_buffer-structure"></a>Estrutura BUFFER DO DBG ORPC \_ \_

A **estrutura BUFFER DO \_ DBG \_ ORPC** é o formato de buffer usado para marshalled de dados RPC para os métodos da interface [**IOrpcDebugNotify.**](iorpcdebugnotify.md)

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _ORPC_DBG_BUFFER {
  DWORD alwaysOrSometimes;
  BYTE  verMajor;
  BYTE  verMinor;
  DWORD cbRemaining;
  GUID  guidSemantic;
  union {
    BOOL   fStopOnOtherSide;
    USHORT wDebuggingOpCode;
    USHORT cExtent;
    BYTE   padding[2];
    struct {
      ULONG cb;
      GUID  guidExtent;
      BYTE  *rgbData;
    };
  };
} ORPC_DBG_BUFFER, *PORPC_DBG_BUFFER;
```



## <a name="members"></a>Membros

<dl> <dt>

**alwaysOrSometimes**
</dt> <dd>

Um valor que controla a depuração do depurador. **alwaysOrSometimes** pode ser um dos seguintes valores:



| Valor                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ORPC_DEBUG_ALWAYS"></span><span id="orpc_debug_always"></span><dl> <dt>**ORPC \_ DEPURAR \_ SEMPRE**</dt> <dt>0X00000000</dt> </dl>                              | Se definido, o COM sempre aumentará a notificação do cliente ou do servidor no receptor.<br/>                                                                                                                                                    |
| <span id="ORPC_DEBUG_IF_HOOK_ENABLED"></span><span id="orpc_debug_if_hook_enabled"></span><dl> <dt>**ORPC \_ DEPURAR \_ SE O GANCHO ESTIVER HABILITADO \_ \_ 0X00000001**</dt> <dt></dt> </dl> | Se definido, o COM só aciona a notificação do cliente ou do servidor no receptor se a depuração COM tiver sido habilitada chamando [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) nesse processo com **fTrace** definido como **TRUE.** <br/> |



 

</dd> <dt>

**verMajor**
</dt> <dd>

O número de versão principal da especificação de formato de dados.

</dd> <dt>

**Verminor**
</dt> <dd>

O número de versão secundária da especificação de formato de dados.

</dd> <dt>

**cbRemaining**
</dt> <dd>

O número de bytes, inclusive **cbRemaining,** que segue nesta estrutura.

</dd> <dt>

**guidSemantic**
</dt> <dd>

Um GUID que determina quais membros da união estão presentes abaixo. **guidSemantic** pode usar um dos seguintes valores:



| Valor                                                                                                           | Significado                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt> </dl> | Determina se uma única ida e volta deve ser executada pelo depurador. Somente o **membro fStopOnOtherSide** da união está presente abaixo.<br/>                                             |
| <dl> <dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt> </dl> | Determina se dados com marshaling de RPC e opcodes de depuração são passados para o receptor. Todos os membros da união estão presentes abaixo, com exceção de **fStopOnOtherSide**.<br/> |



 

</dd> <dt>

**fStopOnOtherSide**
</dt> <dd>

Se **TRUE**, uma única etapa será executada pelo depurador e deverá sair do servidor e continuar a execução depois que o outro lado for atingido. Caso contrário, uma única execução não será executada e a execução do depurador será interrompida no outro lado.

</dd> <dt>

**wDebuggingOpCode**
</dt> <dd>

Um valor que permite que uma de uma série de operações seja especificada. **wDebuggingOpCode** pode usar um dos seguintes valores:



| Valor                                                                             | Significado                                                                                              |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x0000</dt> </dl> | Sem operação.<br/>                                                                             |
| <dl> <dt>0x0001</dt> </dl> | Se definido, a semântica de etapa única será idêntica a **fStopOnOtherSide** quando definida como **TRUE.**<br/> |



 

</dd> <dt>

**cExtent**
</dt> <dd>

Preenchimento. Não use.

</dd> <dt>

**padding**
</dt> <dd>

Preenchimento. Não use.

</dd> <dt>

**Cb**
</dt> <dd>

O tamanho, em bytes dos dados em **rgbData.**

</dd> <dt>

**guidExtent**
</dt> <dd>

Um **GUID** que determina o tipo de dados em **rgbData.** **guidExtent** pode usar um dos seguintes valores:



| Valor                                                                                                           | Significado                                                   |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>53199051-57EB-11ce-A964-00AA006C3706</dt> </dl> | **rgbData** é um ponteiro de interface marshalled.<br/> |



 

</dd> <dt>

**rgbData**
</dt> <dd>

Um buffer **BYTE** usado para passar dados COM com marshaled de RPC entre os depurador de cliente e servidor. O conteúdo de **rgbData** é determinado pelo **GUID** em **guidExtent.**



| Valor guidExtent                     | rgbData contents                                                                                                                                                                                                                                    |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 53199051-57EB-11ce-A964-00AA006C3706 | Um ponteiro de interface marshalled que resulta da chamada [**a CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface). O ponteiro marshalled é convertido em seu ponteiro de interface correspondente usando [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface). |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Os membros dessa estrutura têm alinhamento de 1 byte e são sempre transmitidos em ordem de byte little-endian.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>N/A</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ORPC \_ DBG \_ ALL**](orpc-dbg-all.md)
</dt> <dt>

[**ORPC \_ INIT \_ ARGS**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 






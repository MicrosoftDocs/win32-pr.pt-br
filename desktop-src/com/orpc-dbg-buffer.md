---
title: Estrutura de ORPC_DBG_BUFFER
description: A \_ estrutura de \_ buffer DBG ORPC é o formato de buffer usado para dados RPC empacotados para os métodos da interface IOrpcDebugNotify.
ms.assetid: 444cd3b8-bc7b-425d-9ccc-04fd6c7393b2
keywords:
- COM ORPC_DBG_BUFFER estrutura COM
- COM ponteiro de estrutura de PORPC_DBG_BUFFER COM
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
ms.openlocfilehash: 4dc42251b928207a2b009a18c1d88e94dcf1492a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813323"
---
# <a name="orpc_dbg_buffer-structure"></a>\_Estrutura de \_ buffer DBG ORPC

A estrutura de **\_ \_ buffer DBG ORPC** é o formato de buffer usado para dados RPC empacotados para os métodos da interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

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

Um valor que controla a geração do depurador. **alwaysOrSometimes** pode ser um dos seguintes valores:



| Valor                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ORPC_DEBUG_ALWAYS"></span><span id="orpc_debug_always"></span><dl> <dt>**ORPC \_ Depurar \_ sempre**</dt> <dt>0x00000000</dt> </dl>                              | Se definido, COM sempre gerará a notificação de cliente ou servidor no receptor.<br/>                                                                                                                                                    |
| <span id="ORPC_DEBUG_IF_HOOK_ENABLED"></span><span id="orpc_debug_if_hook_enabled"></span><dl> <dt>**ORPC \_ Depurar \_ se o \_ gancho estiver \_ habilitado**</dt> <dt>0x00000001</dt> </dl> | Se definido, COM irá gerar apenas a notificação de cliente ou servidor no receptor se a depuração COM tiver sido habilitada chamando [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) nesse processo com **FTrace** definido como **true**. <br/> |



 

</dd> <dt>

**verMajor**
</dt> <dd>

O número de versão principal da especificação de formato de dados.

</dd> <dt>

**verMinor**
</dt> <dd>

O número de versão secundária da especificação de formato de dados.

</dd> <dt>

**cbRemaining**
</dt> <dd>

O número de bytes, inclusive de **cbRemaining**, que seguem nessa estrutura.

</dd> <dt>

**guidSemantic**
</dt> <dd>

Um GUID que determina quais membros da União estão presentes abaixo. **guidSemantic** pode usar um dos seguintes valores:



| Valor                                                                                                           | Significado                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt> </dl> | Determina se a depuração única deve ser executada pelo depurador. Somente o membro **fStopOnOtherSide** da União está presente abaixo.<br/>                                             |
| <dl> <dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt> </dl> | Determina se os dados marshalled de RPC e os opcodes de depuração são passados para o receptor. Todos os membros da União estão presentes abaixo, com exceção de **fStopOnOtherSide**.<br/> |



 

</dd> <dt>

**fStopOnOtherSide**
</dt> <dd>

Se for **true**, a depuração única será executada pelo depurador e ele deverá sair do servidor e continuar a execução quando o outro lado for atingido. Caso contrário, a depuração única não será executada e a execução do depurador será interrompida no outro lado.

</dd> <dt>

**wDebuggingOpCode**
</dt> <dd>

Um valor que permite a especificação de uma série de operações. **wDebuggingOpCode** pode usar um dos seguintes valores:



| Valor                                                                             | Significado                                                                                              |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x0000</dt> </dl> | Sem operação.<br/>                                                                             |
| <dl> <dt>0x0001</dt> </dl> | Se definido, a semântica de etapa única será idêntica a **fStopOnOtherSide** quando definida como **true**.<br/> |



 

</dd> <dt>

**cExtent**
</dt> <dd>

Margem. Não use.

</dd> <dt>

**padding**
</dt> <dd>

Margem. Não use.

</dd> <dt>

**CB**
</dt> <dd>

O tamanho, em bytes, dos dados em **rgbData**.

</dd> <dt>

**guidExtent**
</dt> <dd>

Um **GUID** que determina o tipo de dados em **rgbData**. **guidExtent** pode usar um dos seguintes valores:



| Valor                                                                                                           | Significado                                                   |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>53199051-57EB-11ce-A964-00AA006C3706</dt> </dl> | **rgbData** é um ponteiro de interface marshalled.<br/> |



 

</dd> <dt>

**rgbData**
</dt> <dd>

Um buffer de **bytes** usado para passar dados com marshalled de RPC entre os depuradores de cliente e de servidor. O conteúdo de **rgbData** é determinado pelo **GUID** em **guidExtent**.



| Valor de guidExtent                     | conteúdo do rgbData                                                                                                                                                                                                                                    |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 53199051-57EB-11ce-A964-00AA006C3706 | Um ponteiro de interface marshalled que resulta da chamada de [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface). O ponteiro marshalled é convertido em seu ponteiro de interface correspondente usando [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface). |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Esses membros dessa estrutura têm um alinhamento de 1 byte e sempre são transmitidos em ordem de byte little-endian.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>N/A</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ORPC \_ DBG \_ All**](orpc-dbg-all.md)
</dt> <dt>

[**\_argumentos de inicialização ORPC \_**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 






---
title: Estrutura de ORPC_DBG_ALL
description: A \_ estrutura ORPC DBG \_ All é usada para passar parâmetros para os métodos da interface IOrpcDebugNotify.
ms.assetid: 05371beb-9202-40a6-96d2-4b91497e2ee9
keywords:
- COM ORPC_DBG_ALL estrutura COM
- COM ponteiro de estrutura de LPORPC_DBG_ALL COM
topic_type:
- apiref
api_name:
- ORPC_DBG_ALL
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17f5b09e5fe2f668bf2bcd21e2e7fe6f0f766a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085353"
---
# <a name="orpc_dbg_all-structure"></a>\_Estrutura ORPC DBG \_ All

A estrutura **ORPC \_ DBG \_ All** é usada para passar parâmetros para os métodos da interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

> [!Note]  
> Cada método da interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) usa uma combinação diferente dos membros abaixo. Se um membro não for indicado como usado por um método, ele será indefinido quando passado para esse método.

 

## <a name="syntax"></a>Sintaxe


```C++
typedef struct ORPC_DBG_ALL {
  BYTE              *pSignature;
  RPCOLEMESSAGE     *pMessage;
  const IID         *refiid;
  IRpcChannelBuffer *pChannel;
  IUnknown          *pUnkProxyMgr;
  void              *pInterface;
  IUnknown          *pUnkObject;
  HRESULT           hresult;
  void              *pvBuffer;
  ULONG             *cbBuffer;
  ULONG             *lpcbBuffer;
  void              *reserved;
} ORPC_DBG_ALL, *LPORPC_DBG_ALL;
```



## <a name="members"></a>Membros

<dl> <dt>

**pSignature**
</dt> <dd>

Um ponteiro para um buffer de **bytes** que contém:

-   Primeiros quatro bytes: os caracteres ASCII "MARB" na ordem de memória crescente.
-   Próximos 16 bytes: um **GUID** que identifica a notificação que está sendo chamada. Ele contém um dos seguintes:
    1.  [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): 9ED14F80-9673-101A-B07B-00DD01113F11
    2.  [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):D a45f3e0-9673-101A-B07B-00DD01113F11
    3.  [**ClientNotify**](iorpcdebugnotify-clientnotify.md): 4F60E540-9674-101A-B07B-00DD01113F11
    4.  [**ServerNotify**](iorpcdebugnotify-servernotify.md): 1084FA00-9674-101A-B07B-00DD01113F11
    5.  [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): 22080240-9674-101A-B07B-00DD01113F11
    6.  [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md): 2FC09500-9674-101A-B07B-00DD01113F11
-   Próximos quatro bytes: reservados para uso futuro.

> [!Note]
>
> Usado por todos os métodos da interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

 

</dd> <dt>

**pMessage**
</dt> <dd>

Um ponteiro para uma estrutura [**RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) que contém informações de Marshalling de dados RPC.

> [!Note]
>
> Usado pelos métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**refiid**
</dt> <dd>

Um ponteiro para o IID da interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

> [!Note]
>
> Usado pelos métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**pChannel**
</dt> <dd>

Um ponteiro para a interface [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) da implementação do canal RPC com no servidor.

> [!Note]
>
> Usado pelos métodos [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**pUnkProxyMgr**
</dt> <dd>

Um ponteiro para a interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) do objeto envolvido nesta invocação do depurador. Pode ser **NULL**, no entanto, isso reduz a funcionalidade do depurador.

> [!Note]
>
> Usado pelos métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)e [**ClientNotify**](iorpcdebugnotify-clientnotify.md) .

 

</dd> <dt>

**pInterface**
</dt> <dd>

Um ponteiro para a interface COM do método que será invocado por esse RPC. Não deve ser **nulo**.

> [!Note]
>
> Usado pelos métodos [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**pUnkObject**
</dt> <dd>

Deve ser **NULL**.

> [!Note]
>
> Usado pelos métodos [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**resultado**
</dt> <dd>

A finalidade deste membro é alterada para cada uma das notificações abaixo:

[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): o número de bytes que o depurador do cliente transmitirá para o depurador do servidor. Se for zero, nenhuma informação precisará ser transmitida.

[**ClientNotify**](iorpcdebugnotify-clientnotify.md): o **HRESULT** do último RPC.

[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): o número de bytes que o depurador do cliente transmitirá para o depurador do servidor. Se for zero, nenhuma informação precisará ser transmitida.

> [!Note]
>
> Usado pelos métodos [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md)e [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) .

 

</dd> <dt>

**pvBuffer**
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ buffer DBG ORPC**](orpc-dbg-buffer.md) que contém as informações de depuração marshalled RPC. Será indefinido se **cbBuffer** for zero.

> [!Note]
>
> Usado pelos métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**cbBuffer**
</dt> <dd>

O comprimento, em bytes, dos dados apontados por **pvBuffer**.

> [!Note]
>
> Usado pelos métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)e [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**lpcbBuffer**
</dt> <dd>

O número de bytes que o depurador do cliente transmitirá para o depurador do servidor. Se for zero, nenhuma informação precisará ser transmitida. Esse valor substitui o valor retornado em **HRESULT**.

> [!Note]
>
> Usado pelos métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) .

 

</dd> <dt>

**reservado**
</dt> <dd>

Reservado. Não use.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>N/A</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_buffer de DBG ORPC \_**](orpc-dbg-buffer.md)
</dt> <dt>

[**\_argumentos de inicialização ORPC \_**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 


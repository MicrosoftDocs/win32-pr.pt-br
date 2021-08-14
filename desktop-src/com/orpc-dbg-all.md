---
title: ORPC_DBG_ALL estrutura
description: A estrutura ORPC DBG ALL é usada para passar parâmetros para os métodos da \_ \_ interface IOrpcDebugNotify.
ms.assetid: 05371beb-9202-40a6-96d2-4b91497e2ee9
keywords:
- ORPC_DBG_ALL estrutura COM
- LPORPC_DBG_ALL ponteiro de estrutura COM
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
ms.openlocfilehash: 359e3b3ec2530917c6a502da90ea86771238319687f8dcf8e9b7862e4ddf1954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310300"
---
# <a name="orpc_dbg_all-structure"></a>Estrutura ORPC \_ DBG \_ ALL

A **estrutura \_ ORPC DBG \_ ALL** é usada para passar parâmetros para os métodos da interface [**IOrpcDebugNotify.**](iorpcdebugnotify.md)

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

Um ponteiro para um buffer **BYTE** que contém:

-   Primeiros quatro bytes: os caracteres ASCII "MARB" em ordem crescente de memória.
-   Próximos 16 bytes: **um GUID** que identifica a notificação que está sendo chamada. Ele contém um dos seguintes:
    1.  [**ClientGetBufferSize:**](iorpcdebugnotify-clientgetbuffersize.md)9ED14F80-9673-101A-B07B-00DD01113F11
    2.  [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):D A45F3E0-9673-101A-B07B-00DD01113F11
    3.  [**ClientNotify**](iorpcdebugnotify-clientnotify.md):4F60E540-9674-101A-B07B-00DD01113F11
    4.  [**ServerNotify**](iorpcdebugnotify-servernotify.md):1084FA00-9674-101A-B07B-00DD01113F11
    5.  [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md):22080240-9674-101A-B07B-00DD01113F11
    6.  [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md):2FC09500-9674-101A-B07B-00DD01113F11
-   Próximos quatro bytes: Reservado para uso futuro.

> [!Note]
>
> Usado por todos os métodos da interface [**IOrpcDebugNotify.**](iorpcdebugnotify.md)

 

</dd> <dt>

**pMessage**
</dt> <dd>

Um ponteiro para uma [**estrutura RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) que contém informações de marshaling de dados RPC.

> [!Note]
>
> Usado pelos métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer,**](iorpcdebugnotify-serverfillbuffer.md) [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**Refiid**
</dt> <dd>

Um ponteiro para o IID da interface [**IOrpcDebugNotify.**](iorpcdebugnotify.md)

> [!Note]
>
> Usado pelos métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer,**](iorpcdebugnotify-serverfillbuffer.md) [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**pChannel**
</dt> <dd>

Um ponteiro para a interface [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) da implementação do canal COM RPC no servidor.

> [!Note]
>
> Usado pelos [**métodos ServerFillBuffer,**](iorpcdebugnotify-serverfillbuffer.md) [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**pUnkProxyMgr**
</dt> <dd>

Um ponteiro para a interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) do objeto envolvido nesta invocação do depurador. Pode ser **NULL,** no entanto, isso reduz a funcionalidade do depurador.

> [!Note]
>
> Usado pelos [**métodos ClientFillBuffer,**](iorpcdebugnotify-clientfillbuffer.md) [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)e [**ClientNotify.**](iorpcdebugnotify-clientnotify.md)

 

</dd> <dt>

**pInterface**
</dt> <dd>

Um ponteiro para a interface COM do método que será invocado por este RPC. Não deve ser **NULL.**

> [!Note]
>
> Usado pelos [**métodos ServerFillBuffer,**](iorpcdebugnotify-serverfillbuffer.md) [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**Punkobject**
</dt> <dd>

Deve ser **NULL.**

> [!Note]
>
> Usado pelos [**métodos ServerFillBuffer,**](iorpcdebugnotify-serverfillbuffer.md) [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)e [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**Hresult**
</dt> <dd>

A finalidade desse membro muda para cada uma das notificações abaixo:

[**ClientGetBufferSize:**](iorpcdebugnotify-clientgetbuffersize.md)o número de bytes que o depurador do cliente transmitirá para o depurador de servidor. Se zero, nenhuma informação precisará ser transmitida.

[**ClientNotify:**](iorpcdebugnotify-clientnotify.md) **o HRESULT** do último RPC.

[**ServerGetBufferSize:**](iorpcdebugnotify-servergetbuffersize.md)o número de bytes que o depurador do cliente transmitirá para o depurador de servidor. Se zero, nenhuma informação precisará ser transmitida.

> [!Note]
>
> Usado pelos [**métodos ClientGetBufferSize,**](iorpcdebugnotify-clientgetbuffersize.md) [**ClientNotify**](iorpcdebugnotify-clientnotify.md)e [**ServerGetBufferSize.**](iorpcdebugnotify-servergetbuffersize.md)

 

</dd> <dt>

**Pvbuffer**
</dt> <dd>

Um ponteiro para uma estrutura [**\_ BUFFER DO DBG ORPC \_**](orpc-dbg-buffer.md) que contém as informações de depuração com marshall de RPC. Será indefinido se **cbBuffer** for zero.

> [!Note]
>
> Usado pelos [**métodos ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify,**](iorpcdebugnotify-clientnotify.md) [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)e [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**cbBuffer**
</dt> <dd>

O comprimento, em bytes, dos dados apontados por **pvBuffer**.

> [!Note]
>
> Usado pelos [**métodos ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify,**](iorpcdebugnotify-clientnotify.md) [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)e [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**Lpcbbuffer**
</dt> <dd>

O número de bytes que o depurador do cliente transmitirá para o depurador de servidor. Se zero, nenhuma informação precisará ser transmitida. Esse valor é o que é o valor retornado em **hresult**.

> [!Note]
>
> Usado pelos [**métodos ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize.**](iorpcdebugnotify-clientgetbuffersize.md)

 

</dd> <dt>

**Reservados**
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

[**ORPC \_ DBG \_ BUFFER**](orpc-dbg-buffer.md)
</dt> <dt>

[**ORPC \_ INIT \_ ARGS**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 


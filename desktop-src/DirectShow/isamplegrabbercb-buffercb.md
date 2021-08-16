---
description: O método BufferCB é um método de retorno de chamada que recebe um ponteiro para o buffer de exemplo.
ms.assetid: 9ee16dd6-8d05-4a9a-84c3-1b3bb95eaa04
title: Método ISampleGrabberCB::BufferCB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.BufferCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c92e83c8daf5bf129a9aa8330bcc53caa88537f2395aeceebd8b5da2037c5b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817586"
---
# <a name="isamplegrabbercbbuffercb-method"></a>Método ISampleGrabberCB::BufferCB

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O **método BufferCB** é um método de retorno de chamada que recebe um ponteiro para o buffer de exemplo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BufferCB(
   double SampleTime,
   BYTE   *pBuffer,
   long   BufferLen
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SampleTime* 
</dt> <dd>

Hora de início do exemplo, em segundos.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Ponteiro para um buffer que contém os dados de exemplo. O formato dos dados depende do tipo de mídia do pin de entrada do Grabber de exemplo. Para obter o tipo de mídia, chame [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md).

</dd> <dt>

*BufferLen* 
</dt> <dd>

Comprimento do buffer apontado por *pBuffer*, em bytes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se for bem-sucedido ou um **código de erro HRESULT** caso contrário.

## <a name="remarks"></a>Comentários

Esse método de retorno de chamada recebe um ponteiro para os dados no exemplo de mídia mais recente.

> [!Note]  
> Esse método recebe um ponteiro para os dados de exemplo originais, não uma cópia. A documentação original incorretamente declarou que *pBuffer* contém uma cópia dos dados.

 

Para configurar o retorno de chamada, chame [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> <dt>

[**ISampleGrabberCB Interface**](isamplegrabbercb.md)
</dt> </dl>

 

 





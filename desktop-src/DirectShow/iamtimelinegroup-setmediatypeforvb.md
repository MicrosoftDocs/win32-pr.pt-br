---
description: O método SetMediaTypeForVB especifica o tipo de mídia de grupo, para clientes de Automação.
ms.assetid: 86f52088-a0dd-40be-98a0-8adc09b264dd
title: Método IAMTimelineGroup::SetMediaTypeForVB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaTypeForVB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ea47e4edcdfc58e38e61a9f92eb5afac0092ab0cb445f6ff73471e1b65b1480b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905036"
---
# <a name="iamtimelinegroupsetmediatypeforvb-method"></a>Método IAMTimelineGroup::SetMediaTypeForVB

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetMediaTypeForVB` método especifica o tipo de mídia de grupo, para clientes de Automação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMediaTypeForVB(
  [in] long Val
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Val* \[ Em\]
</dt> <dd>

Valor que especifica o tipo de mídia. De definir o valor como 0 para vídeo ou 1 para áudio.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Esse método destina-se a clientes de Automação. Para aplicativos C++, use o [**método IAMTimelineGroup::SetMediaType.**](iamtimelinegroup-setmediatype.md)

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

[**IAMTimelineGroup Interface**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 





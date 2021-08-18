---
description: O método GetMediaTimes recupera os horários de início e parada da mídia.
ms.assetid: c6a7d992-ceb5-4378-aee2-f2d778b41516
title: Método IAMTimelineSrc::GetMediaTimes (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a2a4b3fc716ba0865a010155e2f1e8a592cab396f5efb0c2d4afa3264da4a337
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756036"
---
# <a name="iamtimelinesrcgetmediatimes-method"></a>Método IAMTimelineSrc::GetMediaTimes

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetMediaTimes` método recupera os horários de início e parada da mídia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pstart* 
</dt> <dd>

Recebe a hora de início da mídia, em unidades de 100 nanossegundos.

</dd> <dt>

*pStop* 
</dt> <dd>

Recebe o tempo de parada de mídia, em unidades de 100 nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Os tempos de mídia são relativos ao arquivo de mídia original. Para obter mais informações, consulte [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

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

[**IAMTimelineSrc Interface**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 





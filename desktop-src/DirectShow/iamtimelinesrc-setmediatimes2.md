---
description: O método SetMediaTimes2 define os horários de parada e início da mídia. Esse método é equivalente a IAMTimelineSrc::SetMediaTimes, mas aceita valores REFTIME.
ms.assetid: 9eea7965-46c5-416c-97df-134d29130c8a
title: Método IAMTimelineSrc::SetMediaTimes2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5d94515f2e810f74e788f5d8909ddee377bebee29525cc3d0c12b0463635043e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154898"
---
# <a name="iamtimelinesrcsetmediatimes2-method"></a>Método IAMTimelineSrc::SetMediaTimes2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetMediaTimes2` método define as horas de início e de parada de mídia. Esse método é equivalente a [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md), mas aceita [**valores REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMediaTimes2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Iniciar* 
</dt> <dd>

Hora de início da mídia, em segundos.

</dd> <dt>

*Parar* 
</dt> <dd>

Tempo de parada de mídia, em segundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

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

 

 





---
description: O método SetStretchMode define o modo de alongamento. O modo de alongamento determina como uma fonte de vídeo será renderizada se seu tamanho não corresponder às dimensões de saída.
ms.assetid: 4f720975-5035-4539-895f-3eb3c3b31719
title: Método IAMTimelineSrc::SetStretchMode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c12d14edf665bb3257b627a194923c267ee9e8bd25027e40a7a975a15c10025f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148539"
---
# <a name="iamtimelinesrcsetstretchmode-method"></a>Método IAMTimelineSrc::SetStretchMode

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetStretchMode` método define o modo de alongamento. O modo de alongamento determina como uma fonte de vídeo será renderizada se seu tamanho não corresponder às dimensões de saída.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetStretchMode(
   int nStretchMode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nStretchMode* 
</dt> <dd>

Sinalizador que indica o modo de alongamento atual. Para ver uma lista de valores possíveis, consulte [**Resize Flags**](resize-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

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

 

 





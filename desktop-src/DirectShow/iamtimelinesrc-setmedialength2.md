---
description: O método SetMediaLength2 especifica a duração do arquivo de origem. Esse método é equivalente a IAMTimelineSrc::SetMediaLength, mas obtém um valor REFTIME.
ms.assetid: 1a1dcf23-2041-4791-bce7-0ecbe33df592
title: Método IAMTimelineSrc::SetMediaLength2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2541639841792b5f46f486e602dd8c870b8a90b3c327a7a8f06277c3fdbeb163
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119256646"
---
# <a name="iamtimelinesrcsetmedialength2-method"></a>Método IAMTimelineSrc::SetMediaLength2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetMediaLength2` método especifica a duração do arquivo de origem. Esse método é equivalente a [**IAMTimelineSrc::SetMediaLength,**](iamtimelinesrc-setmedialength.md)mas obtém um [**valor REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMediaLength2(
   REFTIME Length
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Comprimento* 
</dt> <dd>

Comprimento da mídia, em segundos.

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

 

 





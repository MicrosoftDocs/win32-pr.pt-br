---
description: O método GetMediaLength2 recupera o comprimento da mídia desse objeto de origem. Esse método é equivalente a IAMTimelineSrc::GetMediaLength, mas aceita valores REFTIME.
ms.assetid: 96685e00-4e16-4205-a6ad-8b83cf2f8c29
title: Método IAMTimelineSrc::GetMediaLength2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 951e7909d55517489c77190434bf677ccdd8bee8dc1238ecd247d117a551610a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131106"
---
# <a name="iamtimelinesrcgetmedialength2-method"></a>Método IAMTimelineSrc::GetMediaLength2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetMediaLength2` método recupera o comprimento de mídia desse objeto de origem. Esse método é equivalente a [**IAMTimelineSrc::GetMediaLength,**](iamtimelinesrc-getmedialength.md)mas aceita [**valores REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMediaLength2(
   REFTIME *pLength
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pLength* 
</dt> <dd>

Recebe o comprimento da mídia em segundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes **valores HRESULT:**



| Código de retorno                                                                                     | Descrição                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | Êxito.<br/>                                |
| <dl> <dt>**E \_ NOTDETERMINED**</dt> </dl> | Os tempos de mídia não são definidos neste objeto.<br/> |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>       | Argumento de ponteiro **NULL.**<br/>              |



 

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

 

 





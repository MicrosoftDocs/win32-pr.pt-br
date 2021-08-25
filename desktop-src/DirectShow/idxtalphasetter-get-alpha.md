---
description: O método \_ get Alpha recupera o valor alfa para toda a imagem.
ms.assetid: ce891149-e964-4239-aeef-c9f4a8354563
title: Método IDxtAlphaSetter::get_Alpha (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 054e2a1745f96dc4d6ea846bed0448948fae8407dd6ab44d2796742e405f2e1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051966"
---
# <a name="idxtalphasetterget_alpha-method"></a>Método Alfa IDxtAlphaSetter::get \_

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_Alpha` método recupera o valor alfa de toda a imagem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Alpha(
  [out, retval] long *pAlpha
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAlpha* \[ out, retval\]
</dt> <dd>

Recebe o valor alfa. Esse valor alfa será aplicado a toda a imagem de destino. Um valor negativo indica que nenhum valor alfa está definido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os possíveis valores incluem os seguintes.



| Código de retorno                                                                               | Descrição                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl> | **Argumento de** ponteiro NULL<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Êxito<br/>                   |



 

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

[**IDxtAlphaSetter Interface**](idxtalphasetter.md)
</dt> </dl>

 

 





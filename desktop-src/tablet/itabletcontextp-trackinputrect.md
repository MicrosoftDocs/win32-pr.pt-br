---
description: Atualiza o Tablet digitalizador para as coordenadas de mapeamento de local de janela.
ms.assetid: 2984b87b-620e-4e5d-a3cc-4c3f4c89bae3
title: 'Método ITabletContextP:: TrackInputRect'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.TrackInputRect
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 4529263b81933651db35b88262b11e979d39e6f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790372"
---
# <a name="itabletcontextptrackinputrect-method"></a>Método ITabletContextP:: TrackInputRect

Atualiza o Tablet digitalizador para as coordenadas de mapeamento de local de janela.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT TrackInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*prcInput* \[ fora\]
</dt> <dd>

O novo retângulo de janela de entrada depois de atualizar o mapeamento entre as coordenadas de janela e digitalizador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

Chame esse método sempre que o local da janela na tela for alterado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITabletContextP**](itabletcontextp.md)
</dt> </dl>

 

 





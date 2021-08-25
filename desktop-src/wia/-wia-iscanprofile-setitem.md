---
description: Define o GUID da categoria de Windows wia (aquisição de imagem) 2.0 ao que o perfil está associado.
ms.assetid: e359abcb-b5d5-45a4-b650-2b278ba1ff6a
title: Método IScanProfile::SetItem (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: fc4f79c44ff84bef1efbda4b09beee6b7dcf83f04023a5e2211e9f808b18446a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814066"
---
# <a name="iscanprofilesetitem-method"></a>Método IScanProfile::SetItem

Define o GUID da categoria de Windows wia (aquisição de imagem) 2.0 ao que o perfil está associado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetItem(
  [in] GUID guidCategory
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*guidCategory* \[ Em\]
</dt> <dd>

Tipo: **GUID**

O GUID da categoria do item WIA 2.0. Essa deve ser uma das constantes DE CATEGORIA DE \_ ITEM IPA do \_ WIA. \_

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Os usuários podem alterar a categoria com o [**método ScanProfileDialog.**](-wia-iscanprofileui-scanprofiledialog.md)

As alterações em um perfil não são salvas no disco até que o aplicativo chama o [**método IScanProfile::Save.**](-wia-iscanprofile-save.md)

Se dois aplicativos criarem objetos de perfil de verificação do mesmo arquivo XML e cada aplicativo grava alterações em seu objeto, somente as alterações feitas pelo aplicativo que chama [**IScanProfile::Save**](-wia-iscanprofile-save.md) last serão salvas no disco.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>Scanprofile.h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Esquema de perfil de verificação](-wia-scan-profile-schema.md)
</dt> </dl>

 

 





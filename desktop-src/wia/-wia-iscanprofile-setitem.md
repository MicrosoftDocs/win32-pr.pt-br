---
description: Define o GUID da categoria do item de aquisição de imagem do Windows (WIA) 2,0 ao qual o perfil está associado.
ms.assetid: e359abcb-b5d5-45a4-b650-2b278ba1ff6a
title: 'Método IScanProfile:: SetItem (ScanProfile. h)'
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
ms.openlocfilehash: d4b20aae0740656b46dd26824947fc27513afcac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761547"
---
# <a name="iscanprofilesetitem-method"></a>Método IScanProfile:: SetItem

Define o GUID da categoria do item de aquisição de imagem do Windows (WIA) 2,0 ao qual o perfil está associado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetItem(
  [in] GUID guidCategory
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*guidCategory* \[ no\]
</dt> <dd>

Tipo: **GUID**

O GUID da categoria do item WIA 2,0. Deve ser uma das \_ constantes da categoria de item IPA do WIA \_ \_ .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Os usuários podem alterar a categoria com o método [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .

As alterações em um perfil não são salvas no disco até que o aplicativo chame o método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .

Se dois aplicativos criarem objetos de perfil de verificação do mesmo arquivo XML e cada aplicativo gravar alterações em seu objeto, somente as alterações feitas pelo aplicativo que chama [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last serão salvas no disco.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>ScanProfile. h</dt> </dl>    |
| INSERI<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Esquema do perfil de verificação](-wia-scan-profile-schema.md)
</dt> </dl>

 

 





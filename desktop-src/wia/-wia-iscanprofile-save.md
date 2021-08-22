---
description: Salva as alterações em um perfil no disco.
ms.assetid: e844bd4c-93c3-44a3-b7d5-0beb71c9fa17
title: Método IScanProfile::Save (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.Save
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 7cf4201a0d149c7b529e595d7f2c2ea92a6010f6cffd3e6c5c74fb3cdc040651
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450916"
---
# <a name="iscanprofilesave-method"></a>Método IScanProfile::Save

Salva as alterações em um perfil no disco.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Save();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Um perfil de verificação salvo é um arquivo XML armazenado em %USERPROFILE% Dados do \\ Aplicativo Microsoft Document Center \\ \\ \\ UserScanProfiles.

Se mais de um processo grava no objeto [**IScanProfile,**](-wia-iscanprofile.md) aquele que chama **IScanProfile::Save** last é o único processo cujas alterações são salvas.

O **método IScanProfile::Save** valida o perfil antes de salvar. O perfil sempre é considerado válido, a menos que a categoria do item WIA (Aquisição de Imagem) 2.0 do Windows associado ao perfil seja WIA CATEGORY FLATBED ou \_ \_ WIA \_ CATEGORY \_ FEEDER. Se a categoria for WIA CATEGORY FLATBED ou \_ \_ WIA \_ CATEGORY FEEDER, as seguintes propriedades deverão ser válidas para o item, se as propriedades estão contidas \_ no perfil:

BRILHO \_ DE IPS DO WIA \_

CONTRASTE \_ DE IPS DO WIA \_

WIA \_ IPA \_ DATATYPE

WIA \_ IPS \_ XRES

FORMATO \_ IPA DO WIA \_

Além disso, se a categoria for WIA CATEGORY FEEDER, a propriedade TAMANHO DA PÁGINA IPS do WIA deverá ser válida, se ela estiver \_ \_ presente no \_ \_ \_ perfil. Para obter mais informações sobre essas propriedades, consulte [**Constantes de propriedade de item WIA do scanner**](-wia-wiaitempropscanneritem.md).

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

 

 





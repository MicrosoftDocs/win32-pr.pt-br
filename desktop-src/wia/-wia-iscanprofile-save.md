---
description: Salva as alterações em um perfil no disco.
ms.assetid: e844bd4c-93c3-44a3-b7d5-0beb71c9fa17
title: 'Método IScanProfile:: Save (ScanProfile. h)'
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
ms.openlocfilehash: 6d4787380344a7bf8adb70f4cb5a3eaacdea403a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502000"
---
# <a name="iscanprofilesave-method"></a>Método IScanProfile:: Save

Salva as alterações em um perfil no disco.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Save();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Um perfil de verificação salvo é um arquivo XML armazenado em% USERPROFILE% \\ dados de aplicativo \\ Microsoft \\ Document Center \\ UserScanProfiles.

Se mais de um processo gravar no objeto [**IScanProfile**](-wia-iscanprofile.md) , aquele que chama **IScanProfile:: Save** Last será o único processo cujas alterações são salvas.

O método **IScanProfile:: Save** valida o perfil antes de salvar. O perfil é sempre considerado válido, a menos que a categoria do item de aquisição de imagem do Windows (WIA) 2,0 associado ao perfil seja o \_ \_ feed de categoria WIA ou o \_ alimentador de categoria WIA \_ . Se a categoria for o \_ feed de categoria WIA \_ ou o \_ \_ alimentador de categoria WIA, as propriedades a seguir deverão ser válidas para o item, se as propriedades estiverem contidas no perfil:

\_brilho de IPS WIA \_

\_contraste de IPS WIA \_

\_tipo de \_ dados IPA WIA

\_XRES IPS \_ WIA

\_formato IPA \_ WIA

Além disso, se a categoria for o \_ alimentador de categorias WIA \_ , \_ a \_ Propriedade tamanho da página IPS WIA \_ deverá ser válida, se estiver presente no perfil. Para obter mais informações sobre essas propriedades, consulte [**constantes de Propriedade do item WIA do scanner**](-wia-wiaitempropscanneritem.md).

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

 

 





---
description: A interface IScanProfileMgr fornece métodos para criar, abrir, excluir e gerenciar perfis de verificação.
ms.assetid: f57a71b7-750c-42a8-be73-229f0145d9d5
title: Interface IScanProfileMgr (Scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 9f0762befdda272b91451dcca67c3f9560ad354e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757055"
---
# <a name="iscanprofilemgr-interface"></a>Interface IScanProfileMgr

A interface **IScanProfileMgr** fornece métodos para criar, abrir, excluir e gerenciar perfis de verificação.

## <a name="members"></a>Membros

A interface **IScanProfileMgr** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IScanProfileMgr** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IScanProfileMgr** tem esses métodos.



| Método                                                                              | Descrição                                                                                                            |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md)                         | Cria um perfil de verificação vazio e o associa a um scanner ou a outro item WIA 2,0.<br/>                       |
| [**DeleteAllProfiles**](-wia-iscanprofilemgr-deleteallprofiles.md)                 | Exclui todos os perfis de verificação associados ao dispositivo especificado.<br/>                                         |
| [**DeleteAllProfilesForUser**](-wia-iscanprofilemgr-deleteallprofilesforuser.md)   | Exclui todos os perfis de verificação disponíveis para o usuário no sistema em que seu aplicativo está sendo executado. <br/> |
| [**DeleteProfile**](-wia-iscanprofilemgr-deleteprofile.md)                         | Exclui o perfil de exame especificado.<br/>                                                                         |
| [**GetDefaultProfile**](-wia-iscanprofilemgr-getdefaultprofile.md)                 | Obtém o perfil de exame padrão.<br/>                                                                              |
| [**GetNumProfiles**](-wia-iscanprofilemgr-getnumprofiles.md)                       | Obtém o número de perfis de verificação criados para o usuário no sistema em que seu aplicativo está sendo executado.<br/> |
| [**GetNumProfilesforDeviceID**](-wia-iscanprofilemgr-getnumprofilesfordeviceid.md) | Obtém o número de perfis de verificação para o dispositivo.<br/>                                                            |
| [**Getperfis**](-wia-iscanprofilemgr-getprofiles.md)                             | Obtém todos os perfis de verificação disponíveis para o usuário no sistema em que seu aplicativo está sendo executado.<br/>     |
| [**GetProfilesforDeviceID**](-wia-iscanprofilemgr-getprofilesfordeviceid.md)       | Obtém todos os perfis de verificação associados a um dispositivo.<br/>                                                        |
| [**OpenProfile**](-wia-iscanprofilemgr-openprofile.md)                             | Abre um perfil de verificação que foi salvo no disco como um arquivo XML.<br/>                                            |
| [**Atualizar**](-wia-iscanprofilemgr-refresh.md)                                     | Enumera novamente todos os perfis de verificação no sistema.<br/>                                                          |
| [**SetDefault**](-wia-iscanprofilemgr-setdefault.md)                               | Define o perfil de verificação especificado como o perfil padrão.<br/>                                                     |



 

## <a name="remarks"></a>Comentários

Para criar um objeto **IScanProfileMgr** , use o método [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com os seguintes parâmetros:

``` syntax
CoCreateInstance(CLSID_ScanProfileMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IScanProfileMgr, ppv)
```

Se um perfil de verificação for salvo usando o método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) , ele será armazenado como um arquivo XML em% USERPROFILE% \\ dados de aplicativo \\ Microsoft \\ Document Center \\ UserScanProfiles.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Scanprofilemgr. h</dt> </dl> |
| INSERI<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Esquema do perfil de verificação](-wia-scan-profile-schema.md)
</dt> </dl>

 

 

---
description: A interface IScanProfile representa um único perfil de verificação e permite que os aplicativos definam e obtenham as propriedades do perfil.
ms.assetid: 5cd76256-d64e-4934-8cc2-0a467c7e34a9
title: Interface IScanProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile
api_type:
- COM
api_location:
- Scanprofiles.idl
ms.openlocfilehash: 2e02352eef16a9b899e4c635f11c5d10b3ab5113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764404"
---
# <a name="iscanprofile-interface"></a>Interface IScanProfile

A interface **IScanProfile** representa um único perfil de verificação e permite que os aplicativos definam e obtenham as propriedades do perfil.

## <a name="members"></a>Membros

A interface **IScanProfile** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IScanProfile** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IScanProfile** tem esses métodos.



| Método                                                     | Descrição                                                                                                                                         |
|:-----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAllPropIDs**](-wia-iscanprofile-getallpropids.md)   | Obtém todas as IDs de propriedade disponíveis em um perfil.<br/>                                                                                            |
| [**GetDeviceID**](-wia-iscanprofile-getdeviceid.md)       | Retorna a ID do dispositivo.<br/>                                                                                                            |
| [**GetGUID**](-wia-iscanprofile-getguid.md)               | Retorna o GUID do perfil.<br/>                                                                                                         |
| [**GetItem**](-wia-iscanprofile-getitem.md)               | Obtém o GUID da categoria do item WIA 2,0 ao qual o perfil está associado.<br/>                                                   |
| [**GetName**](-wia-iscanprofile-getname.md)               | Obtém o nome amigável do perfil.<br/>                                                                                                   |
| [**GetNumPropIDS**](-wia-iscanprofile-getnumpropids.md)   | Obtém o número de IDs de propriedade em um perfil.<br/>                                                                                            |
| [**GetProperty**](-wia-iscanprofile-getproperty.md)       | Obtém o valor das propriedades filho especificadas no `<Properties>` elemento de um perfil de verificação.<br/>                                            |
| [**IsDefault**](-wia-iscanprofile-isdefault.md)           | Obtém um valor que indica se o perfil é o perfil de exame padrão de um dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) associado.<br/> |
| [**Removerproperty**](-wia-iscanprofile-removeproperty.md) | Remove uma lista especificada de propriedades filho no `<Properties>` elemento de um perfil de verificação.<br/>                                            |
| [**Salvar**](-wia-iscanprofile-save.md)                     | Salva as alterações em um perfil no disco.<br/>                                                                                                      |
| [**SetItem**](-wia-iscanprofile-setitem.md)               | Define o GUID da categoria do item WIA 2,0 ao qual o perfil está associado.<br/>                                                       |
| [**SetName**](-wia-iscanprofile-setname.md)               | Define o nome amigável do perfil.<br/>                                                                                                   |
| [**SetProperty**](-wia-iscanprofile-setproperty.md)       | Define o valor das propriedades filho especificadas no `<Properties>` elemento de um perfil de verificação.<br/>                                            |



 

## <a name="remarks"></a>Comentários

Qualquer dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) pode ter um perfil de verificação. No entanto, **IWiaItem2** itens dos \_ tipos \_ grupo WIA concluído \_ arquivo e \_ raiz da categoria WIA \_ não podem ter perfis.

Se um perfil de verificação for salvo usando o método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) , ele será armazenado como um arquivo XML em% USERPROFILE% \\ dados de aplicativo \\ Microsoft \\ Document Center \\ UserScanProfiles.

Para criar uma instância de um objeto **IScanProfile** , use o método [**IScanProfileMgr:: CreateProfile**](-wia-iscanprofilemgr-createprofile.md) . Para obter uma referência a um perfil de verificação que já foi salvo no disco, use o método [**IScanProfileMgr:: OpenProfile**](-wia-iscanprofilemgr-openprofile.md) .

Todos os perfis de verificação têm os seguintes elementos: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` e `<Properties>` . O perfil padrão de um dispositivo também tem um `<Default>` elemento.

Os `<ProfileGUID>` `<DeviceID>` elementos e não podem ser alterados depois que o perfil é criado. Os valores do `<ProfileName>` elemento e do `<WiaItem>` elemento podem ser alterados depois que o perfil é criado. O `<Default>` elemento pode ser adicionado ou excluído. Isso pode ser feito de forma programática com os métodos [**IScanProfile:: SetName**](-wia-iscanprofile-setname.md), [**IScanProfile:: SetItem**](-wia-iscanprofile-setitem.md)e [**IScanProfileMgr:: SetDefault**](-wia-iscanprofilemgr-setdefault.md) . Essas propriedades também podem ser alteradas pelos usuários por meio do método [**IScanProfileUI:: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .

O `<Properties>` elemento contém `<Property>` filhos. Use-os para adicionar qualquer propriedade de dispositivo ou item WIA 2,0 ao perfil. Você também pode desenvolver sua própria imagem aquisição `<Property>` filhos. Isso torna o esquema do perfil de verificação extensível. (Para obter mais informações sobre como estender o esquema, consulte [definindo propriedades personalizadas](-wia-defining-custom-properties.md), [**IScanProfile:: GetProperty**](-wia-iscanprofile-getproperty.md)e [**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md).)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                        |
| INSERI<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Esquema do perfil de verificação](-wia-scan-profile-schema.md)
</dt> </dl>

 

 

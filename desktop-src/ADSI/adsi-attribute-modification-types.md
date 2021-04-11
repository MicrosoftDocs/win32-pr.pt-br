---
title: Tipos de modificação de atributo ADSI (IADs. h)
description: Usado com o membro dwControlCode da \_ estrutura de informações attr do ADS \_ para especificar o tipo de operação a ser executada quando um atributo é modificado com o método IDirectoryObject setobjectattributes.
ms.assetid: e9a454c8-e067-4730-97f4-85c4f5889e05
ms.tgt_platform: multiple
keywords:
- ADSI tipos de modificação de atributo
topic_type:
- apiref
api_name:
- ADS_ATTR_CLEAR
- ADS_ATTR_UPDATE
- ADS_ATTR_APPEND
- ADS_ATTR_DELETE
api_location:
- Iads.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a739241fd52a7d45d58a1b36bb7de838234d6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009080"
---
# <a name="adsi-attribute-modification-types"></a>Tipos de modificação de atributo ADSI

As constantes a seguir são usadas com o membro **dwControlCode** da estrutura de [**\_ \_ informações attr do ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) para especificar o tipo de operação a ser executada quando um atributo é modificado com o método [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) . Para obter mais informações sobre como usar esses valores, consulte [modificando atributos com ADSI](modifying-attributes-with-adsi.md).

<dl> <dt>

<span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**\_atributo attr do ADS \_ Clear**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Faz com que todos os valores de atributo sejam removidos de um objeto.


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**\_atualização de attr ADS \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Faz com que os valores de atributo especificados sejam atualizados.


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**\_atributo attr do ADS \_ Append**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Faz com que os valores de atributo especificados sejam acrescentados aos valores de atributo existentes.


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**\_exclusão de attr ADS \_**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Faz com que os valores de atributo especificados sejam removidos de um objeto.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Essas constantes devem ser usadas com a estrutura de [**\_ \_ informações attr do ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) no método [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) . Essas constantes não devem ser confundidas com membros da [**enumeração \_ \_ \_ enum da operação de propriedade ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) , que devem ser usadas com o método [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                    |
| parâmetro<br/>                   | <dl> <dt>IADs. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_informações de attr ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)
</dt> <dt>

[**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)
</dt> <dt>

[Modificando atributos com ADSI](modifying-attributes-with-adsi.md)
</dt> </dl>

 

 






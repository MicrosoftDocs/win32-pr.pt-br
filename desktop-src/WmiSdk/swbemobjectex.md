---
description: Fornece funcionalidade estendida para SWbemObject. Como SWbemObject, os métodos desse objeto estendido podem ser usados por todos os objetos WMI.
ms.assetid: 944d4cdc-ad35-4b53-b755-f10131a087fb
ms.tgt_platform: multiple
title: Objeto SWbemObjectEx (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx
- SetFromText_
- ISWbemObjectEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 642b76cde4f4e27979dae0e930ec987dc9a02d36aa8d17c7dcdd9b8785204ac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860146"
---
# <a name="swbemobjectex-object"></a>Objeto SWbemObjectEx

O objeto **SWbemObjectEx** fornece funcionalidade estendida para [**SWbemObject**](swbemobject.md). Como **SWbemObject**, os métodos desse objeto estendido podem ser usados por todos os objetos WMI. Este objeto não pode ser criado pela chamada VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .

## <a name="members"></a>Membros

O objeto **SWbemObjectEx** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SWbemObjectEx** tem esses métodos.



| Método                                      | Descrição                                                              |
|:--------------------------------------------|:-------------------------------------------------------------------------|
| [**GetText\_**](swbemobjectex-gettext-.md) | Retorna um arquivo de texto mostrando o conteúdo de um objeto em XML.<br/> |
| [**Atualizar\_**](swbemobjectex-refresh-.md) | Atualiza os dados em um objeto.<br/>                                  |
| **SetFromText\_**                           | Reservado para uso futuro.<br/>                                      |



 

### <a name="properties"></a>Propriedades

O objeto **SWbemObjectEx** tem essas propriedades.



| Propriedade                                                                 | Tipo de acesso           | Descrição                                                                                                                                              |
|:-------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SystemProperties\_**](swbemobjectex-systemproperties-.md)<br/> | Leitura/gravação<br/> | Um objeto [**SWbemPropertySet**](swbempropertyset.md) que contém a coleção de propriedades do sistema que se aplicam ao **SWbemObjectEx**.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECTEX CLSID<br/>                                                         |
| IID<br/>                      | ISWbemObjectEx de IID \_<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[WbemObjectTextFormatEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> </dl>

 


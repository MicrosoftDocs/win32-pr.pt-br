---
description: O objeto SWbemPrivilege representa um único privilégio. Este objeto não pode ser criado pela chamada VBScript CreateObject.
ms.assetid: 18ee4587-6347-4075-b5e9-c5fb02f3cbf7
ms.tgt_platform: multiple
title: Objeto SWbemPrivilege (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege
- ISWbemPrivilege
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c3be448b4088011cd4d628a7d98b448af550b010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011752"
---
# <a name="swbemprivilege-object"></a>Objeto SWbemPrivilege

O objeto **SWbemPrivilege** representa um único privilégio. Este objeto não pode ser criado pela chamada VBScript **CreateObject** .

## <a name="members"></a>Membros

O objeto **SWbemPrivilege** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **SWbemPrivilege** tem essas propriedades.



| Propriedade                                                     | Tipo de acesso           | Descrição                                                                      |
|:-------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------|
| [**DisplayName**](swbemprivilege-displayname.md)<br/> | Somente leitura<br/>  | Nome de exibição deste privilégio.<br/>                                       |
| [**Identificador**](swbemprivilege-identifier.md)<br/>   | Leitura/gravação<br/> | Inteiro que representa o privilégio que está sendo definido ou recuperado.<br/> |
| [**IsEnabled**](swbemprivilege-isenabled.md)<br/>     | Leitura/gravação<br/> | Valor booliano que indica se esse privilégio está habilitado.<br/>            |
| [**Nome**](swbemprivilege-name.md)<br/>               | Somente leitura<br/>  | Nome deste privilégio.<br/>                                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPRIVILEGE CLSID<br/>                                                        |
| IID<br/>                      | ISWbemPrivilege de IID \_<br/>                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Executando operações privilegiadas](executing-privileged-operations.md)
</dt> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

 





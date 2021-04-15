---
description: Você pode usar as propriedades do objeto SWbemMethod para inspecionar uma única definição de método de um objeto WMI. Este objeto não pode ser criado pela chamada VBScript CreateObject.
ms.assetid: 461d5c41-4930-40cf-96e2-bc8cae335b60
ms.tgt_platform: multiple
title: Objeto SWbemMethod (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod
- ISWbemMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 055957bf2774fc1e5c2e1f0149b00ece7b0a1bea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505672"
---
# <a name="swbemmethod-object"></a>Objeto SWbemMethod

Você pode usar as propriedades do objeto **SWbemMethod** para inspecionar uma única definição de método de um objeto WMI. Este objeto não pode ser criado pela chamada VBScript **CreateObject** .

Esse objeto pode ser usado para inspecionar as definições de métodos. Para invocar os métodos, você deve usar o acesso direto (consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md)) em um objeto [**SWbemObject**](swbemobject.md) (que é o mecanismo recomendado) ou a chamada de [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) .

> [!Note]  
> Nesta versão da API, não há suporte para o acesso de gravação para informações de método. Se você quiser definir métodos ou modificar definições de método existentes, poderá definir as alterações de método em um arquivo MOF e enviar as alterações usando o [compilador MOF](compiling-mof-files.md). Como alternativa, use a [API com para o WMI](com-api-for-wmi.md).

 

## <a name="members"></a>Membros

O objeto **SWbemMethod** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **SWbemMethod** tem essas propriedades.



| Propriedade                                                      | Tipo de acesso          | Descrição                                                                                                                        |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**Inparâmetros**](swbemmethod-inparameters.md)<br/>   | Somente leitura<br/> | Um objeto [**SWbemObject**](swbemobject.md) cujas propriedades definem os parâmetros de entrada para esse método.<br/>              |
| [**Nome**](swbemmethod-name.md)<br/>                   | Somente leitura<br/> | O nome do método.<br/>                                                                                                     |
| [**Ter**](swbemmethod-origin.md)<br/>               | Somente leitura<br/> | Classe de origem do método.<br/>                                                                                        |
| [**Parameters**](swbemmethod-outparameters.md)<br/> | Somente leitura<br/> | Um objeto [**SWbemObject**](swbemobject.md) cujas propriedades definem os parâmetros de saída e o tipo de retorno desse método.<br/> |
| [**Qualificadores\_**](swbemmethod-qualifiers-.md)<br/>    | Somente leitura<br/> | Um objeto [**SWbemQualifierSet**](swbemqualifierset.md) que contém os qualificadores para este método.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMMETHOD CLSID<br/>                                                           |
| IID<br/>                      | ISWbemMethod de IID \_<br/>                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

 





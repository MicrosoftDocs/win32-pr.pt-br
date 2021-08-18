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
ms.openlocfilehash: c750e81a3e41450e8cd32f37ccab6fee2f08439c6bc8fc8ae18bf0e4f106b551
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732656"
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
| [**Origem**](swbemmethod-origin.md)<br/>               | Somente leitura<br/> | Classe de origem do método.<br/>                                                                                        |
| [**Parameters**](swbemmethod-outparameters.md)<br/> | Somente leitura<br/> | Um objeto [**SWbemObject**](swbemobject.md) cujas propriedades definem os parâmetros de saída e o tipo de retorno desse método.<br/> |
| [**Qualificadores\_**](swbemmethod-qualifiers-.md)<br/>    | Somente leitura<br/> | Um objeto [**SWbemQualifierSet**](swbemqualifierset.md) que contém os qualificadores para este método.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMMETHOD CLSID<br/>                                                           |
| IID<br/>                      | ISWbemMethod de IID \_<br/>                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

 





---
description: Você pode usar os métodos e as propriedades do objeto SWbemObject para representar uma definição de classe de Instrumentação de Gerenciamento do Windows (WMI) ou uma instância de objeto.
ms.assetid: d303ec1a-5e0c-4a5e-8ed3-ed353a138755
ms.tgt_platform: multiple
title: Objeto SWbemObject (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject
- ISWbemObject
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 287395b976177170c8bdffa0e1817a8755a4d397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813612"
---
# <a name="swbemobject-object"></a>Objeto SWbemObject

Você pode usar os métodos e as propriedades do objeto **SWbemObject** para representar uma definição de classe de instrumentação de gerenciamento do Windows (WMI) ou uma instância de objeto. Este objeto não pode ser criado pela chamada VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .

Este objeto dá suporte a dois tipos de propriedades e métodos. Aqueles definidos nesta seção são propriedades genéricas e métodos que se aplicam a todos os objetos WMI. Além disso, esse objeto expõe as propriedades e os métodos do objeto subjacente como propriedades de automação dinâmica e métodos de **SWbemObject**. Os nomes e os tipos dessas propriedades e métodos dependem do objeto WMI subjacente. Para obter mais informações sobre como esses métodos e propriedades dinâmicas são expostos, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).

Da perspectiva do cliente WMI, esse objeto está sempre em processo. As operações de gravação afetam apenas a cópia local do objeto e as operações de leitura sempre recuperam valores da cópia local. As atualizações para o WMI são executadas somente quando objetos inteiros são gravados usando uma chamada para o método [**SWbemObject. put \_**](swbemobject-put-.md) . Se você modificar as propriedades ou métodos em um objeto **SWbemObject** , suas alterações não serão gravadas no WMI até que você chame **SWbemObject \_ . put**.

O método genérico e os nomes de propriedade definidos nesta seção sempre terminam com um sublinhado à direita (" \_ ") para diferenciá-los dos métodos e propriedades dinâmicos do WMI do objeto subjacente.

Observe que **SWbemObject** não pode ser criado usando o VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx). Method. Se você quiser criar uma nova classe vazia, use [**SWbemServices. Get**](swbemservices-get.md) com um parâmetro de caminho vazio. Essa chamada retorna um objeto **SWbemObject** vazio que pode se tornar uma classe. Em seguida, você pode fornecer um nome de classe para a propriedade de [**classe**](swbemobjectpath-class.md) do objeto [**SWbemObjectPath**](swbemobjectpath.md) retornado pela chamada de [**caminho \_**](swbemobject-path-.md) . Adicione Propriedades à nova classe pelo método [**Properties \_**](swbemobject-properties-.md) . Para criar uma instância, chame **GetObject** na nova classe.

O exemplo de código a seguir mostra como obter uma nova classe e adicionar uma propriedade a ela. O objeto **SWbemObject** que representa a classe deve ser gravado no repositório WMI por uma chamada para [**Put \_**](swbemobject-put-.md).


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path

```



Você pode examinar o repositório com uma ferramenta de exibição, como o [CIM Studio](further-information.md) , para verificar se a nova classe e a instância são exibidas. Para obter um exemplo de como remover uma classe e uma instância do repositório, consulte [**SWbemServices. Delete**](swbemservices-delete.md) ou [**SWbemObject \_ . Delete**](swbemobject-delete-.md).

## <a name="members"></a>Membros

O objeto **SWbemObject** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SWbemObject** tem esses métodos.



| Método                                                        | Descrição                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ASSOCIADORES\_**](swbemobject-associators-.md)             | Recupera os associadores do objeto.<br/>                                                     |
| [**AssociatorsAsync\_**](swbemobject-associatorsasync-.md)   | Recupera de forma assíncrona os associadores do objeto.<br/>                                      |
| [**8i\_**](swbemobject-clone-.md)                         | Faz uma cópia do objeto atual.<br/>                                                          |
| [**CompareTo\_**](swbemobject-compareto-.md)                 | Testa dois objetos para igualdade.<br/>                                                              |
| [**Excluir\_**](swbemobject-delete-.md)                       | Exclui o objeto do WMI.<br/>                                                                 |
| [**DeleteAsync\_**](swbemobject-deleteasync-.md)             | Exclui de forma assíncrona o objeto do WMI.<br/>                                                  |
| [**ExecMethod\_**](swbemobject-execmethod-.md)               | Executa um método exportado por um provedor de método.<br/>                                             |
| [**ExecMethodAsync\_**](swbemobject-execmethodasync-.md)     | Executa de forma assíncrona um método exportado por um provedor de métodos.<br/>                              |
| [**GetObjectText\_**](swbemobject-getobjecttext-.md)         | Recupera a representação textual do objeto (sintaxe MOF).<br/>                             |
| [**Instâncias\_**](swbemobject-instances-.md)                 | Retorna uma coleção de instâncias do objeto (que deve ser uma classe WMI).<br/>                 |
| [**InstancesAsync\_**](swbemobject-instancesasync-.md)       | De forma assíncrona retorna uma coleção de instâncias do objeto (que deve ser uma classe WMI).<br/>  |
| [**Posicione\_**](swbemobject-put-.md)                             | Cria ou atualiza o objeto no WMI.<br/>                                                        |
| [**PutAsync\_**](swbemobject-putasync-.md)                   | Cria ou atualiza de forma assíncrona o objeto no WMI.<br/>                                         |
| [**Referências\_**](swbemobject-references-.md)               | Retorna referências ao objeto.<br/>                                                            |
| [**ReferencesAsync\_**](swbemobject-referencesasync-.md)     | De forma assíncrona retorna referências ao objeto.<br/>                                             |
| [**SpawnDerivedClass\_**](swbemobject-spawnderivedclass-.md) | Cria uma nova classe derivada do objeto atual (que deve ser uma classe WMI).<br/>             |
| [**SpawnInstance\_**](swbemobject-spawninstance-.md)         | Cria uma nova instância do objeto atual.<br/>                                              |
| [**Subclasses\_**](swbemobject-subclasses-.md)               | Retorna uma coleção de subclasses do objeto (que deve ser uma classe WMI).<br/>                |
| [**SubclassesAsync\_**](swbemobject-subclassesasync-.md)     | De forma assíncrona retorna uma coleção de subclasses do objeto (que deve ser uma classe WMI).<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **SWbemObject** tem essas propriedades.



| Propriedade                                                   | Tipo de acesso          | Descrição                                                                                                                                |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Derivação\_**](swbemobject-derivation-.md)<br/> | Somente leitura<br/> | Contém uma matriz de cadeias de caracteres que descreve a hierarquia de derivação para a classe.<br/>                                             |
| [**Métodos\_**](swbemobject-methods-.md)<br/>       | Somente leitura<br/> | Um objeto [**SWbemMethodSet**](swbemmethodset.md) que é a coleção de métodos para esse objeto.<br/>                           |
| [**Caminho\_**](swbemobject-path-.md)<br/>             | Somente leitura<br/> | Contém um objeto [**SWbemObjectPath**](swbemobjectpath.md) que representa o caminho do objeto da classe ou instância atual.<br/> |
| [**Propriedades\_**](swbemobject-properties-.md)<br/> | Somente leitura<br/> | Um objeto [**SWbemPropertySet**](swbempropertyset.md) que é a coleção de propriedades deste objeto.<br/>                    |
| [**Qualificadores\_**](swbemobject-qualifiers-.md)<br/> | Somente leitura<br/> | Um objeto [**SWbemQualifierSet**](swbemqualifierset.md) que é a coleção de qualificadores para este objeto.<br/>                  |
| [**Segurança\_**](swbemobject-security-.md)<br/>     | Somente leitura<br/> | Contém um objeto [**SWbemSecurity**](swbemsecurity.md) usado para ler ou alterar as configurações de segurança.<br/>                         |



 

## <a name="examples"></a>Exemplos

A [lista de todas as propriedades e métodos de um](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) exemplo de código VBScript da classe WMI na galeria do TechNet usa o SWbemObject para listar todos os métodos e propriedades de uma classe WMI especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | ISWbemObject de IID \_<br/>                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 


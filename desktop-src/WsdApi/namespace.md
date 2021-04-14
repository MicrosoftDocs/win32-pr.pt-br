---
description: Descreve um namespace.
ms.assetid: 8e31526a-639f-481b-91f1-fcd376818cbf
title: elemento nameSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a8747a25988b880d5287d959273fa0f4d144045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505703"
---
# <a name="namespace-element"></a>elemento nameSpace

Descreve um namespace. Esse namespace pode ser usado para geração de código ou para manipular <as diretivas WSDL: Import>.

## <a name="usage"></a>Uso

``` syntax
<nameSpace
  uri = "character_string">
  child elements
</nameSpace>
```

## <a name="attributes"></a>Atributos



| Atributo          | Type                         | Obrigatório       | Descrição                                             |
|--------------------|------------------------------|----------------|---------------------------------------------------------|
| **uri**<br/> | Cadeia de caracteres \_<br/> | Yes<br/> | O URI exclusivo do namespace.<br/> <br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                               | Descrição                                                                                              |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**Codinome**](codename.md)<br/>               | O nome a ser usado para identificar o namespace no código gerado.<br/> <br/>                  |
| [**macroPrefix**](macroprefix.md)<br/>         | O prefixo a ser usado no código gerado para nomes de macros no namespace.<br/> <br/> |
| [**nomes**](name.md)<br/>                       | Um nome qualificado no namespace.<br/> <br/>                                                |
| [**preferredPrefix**](preferredprefix.md)<br/> | O prefixo ao qual o namespace deve ser mapeado para tornar o XML mais legível.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  preferredPrefix?, 
  macroPrefix?, 
  codeName?, 
  name*
)
```

## <a name="parent-elements"></a>Elementos pai



| Elemento                                     | Descrição                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | O elemento raiz de um arquivo de script XML do gerador de código WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse elemento pode ser usado para fornecer ao gerador de código informações adicionais sobre namespaces que ele encontra em arquivos WSDL e XSD ou para introduzir novos namespaces.

Os namespaces implícitos por reflexão de tipo ou especificados em arquivos WSDL e XSD são analisados automaticamente pelo gerador de código e não precisam ser definidos explicitamente no script. Em alguns casos, esse elemento pode ser usado para adicionar propriedades ou nomes adicionais a um namespace que é referenciado por reflexão de tipo ou WSDL/XSD. O gerador de código não considera isso como um conflito.

O XML a seguir mostra um elemento de nameSpace (com filhos omitidos para fins de brevidade).

``` syntax
<nameSpace uri="https://www.example.com/namespace">
  ...
</nameSpace>
```

## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 





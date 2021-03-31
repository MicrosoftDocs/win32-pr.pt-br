---
title: atributo helpstringdll
description: O atributo \ helpstringdll \ define o nome da DLL a ser usada para executar uma pesquisa de cadeia de caracteres de documento.
ms.assetid: 1b9b962c-c355-4428-b5ea-dc7fd48b50a9
keywords:
- helpstringdll do atributo MIDL
topic_type:
- apiref
api_name:
- helpstringdll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dace4fb9ddc3908ce637cd2d8521a1ab4671d620
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917203"
---
# <a name="helpstringdll-attribute"></a>atributo helpstringdll

O atributo **\[ helpstringdll \]** define o nome da dll a ser usada para executar uma pesquisa de cadeia de caracteres de documento.

``` syntax
[
    helpstringdll(help-text-string)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
};
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ajuda-texto-cadeia de caracteres* 
</dt> <dd>

Uma cadeia de caracteres terminada em zero especificando o nome de arquivo totalmente qualificado de uma DLL.

</dd> <dt>

*lista de atributos opcionais* 
</dt> <dd>

Outros atributos que se aplicam à instrução da biblioteca como um todo.

</dd> <dt>

*nome da biblioteca* 
</dt> <dd>

O identificador que os componentes de software usarão para denotar essa [**biblioteca**](library.md).

</dd> <dt>

*bibliotecas-definição-instruções* 
</dt> <dd>

Uma ou mais instruções MIDL que definem a interface da [**biblioteca**](library.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Use o atributo **\[ helpstringdll \]** em uma instrução de biblioteca para especificar, como uma cadeia de caracteres, o nome de arquivo totalmente qualificado de uma biblioteca de vínculo dinâmico. Isso permite que um usuário exiba uma descrição da DLL com o Visualizador de objetos.

Use as funções **GetDocumentation2** nas interfaces **ITypeLib2** e **ITypeInfo2** para recuperar a cadeia de caracteres de ajuda.

## <a name="see-also"></a>Consulte também

<dl> <dt>

[**biblioteca**](library.md)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 
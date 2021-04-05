---
title: atributo version
description: O atributo \ version \ interface identifica uma versão específica entre várias versões de uma interface RPC. Com o atributo Version, você garante que apenas as versões compatíveis do software cliente e do servidor tenham permissão para ligar.
ms.assetid: 66ac5cf3-2230-44fd-aaf6-8013e4a4ae81
keywords:
- MIDL do atributo de versão
topic_type:
- apiref
api_name:
- version
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bacbf7478ebfb745e5fc9b5e50959d0f1587dedf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006570"
---
# <a name="version-attribute"></a>atributo version

O atributo de interface da **\[ versão \]** identifica uma versão específica entre várias versões de uma interface RPC. Com o atributo Version, você garante que apenas as versões compatíveis do software cliente e do servidor tenham permissão para ligar.

``` syntax
version ( major-value[[. minor-value]] )
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor principal* 
</dt> <dd>

Especifica um inteiro não assinado curto entre zero e 65.535, inclusive, que representa o número de versão principal.

</dd> <dt>

*valor secundário* 
</dt> <dd>

Especifica um inteiro não assinado curto entre zero e 65.535, inclusive, que representa o número de versão secundária. O valor da versão secundária é opcional. Se estiver presente, o valor da versão secundária será separado do número de versão principal por um caractere de ponto (.). Se não for especificado, o valor da versão secundária será zero.

</dd> </dl>

## <a name="remarks"></a>Comentários

O compilador MIDL não oferece suporte a várias versões de uma interface COM. Como resultado, uma lista de atributos de interface que inclui o **\[** [](object.md) **\]** atributo Object não pode incluir o atributo **\[ version \]** . Para criar uma nova versão de uma interface COM existente, use a herança de interface. Uma interface COM derivada tem um UUID diferente, mas herda as funções de membro de interface, os códigos de status e os atributos de interface da interface base.

Em combinação com o **\[** valor do [**UUID**](uuid.md) **\]** , o valor da **\[ versão \]** identifica exclusivamente a interface. A biblioteca de tempo de execução passa os valores de **\[ versão \]** e **\[ UUID \]** para o servidor quando o cliente chama uma função remota. Um cliente pode se associar a um servidor para uma determinada interface se:

-   O valor do **\[ UUID \]** é o mesmo.
-   O número de versão principal é o mesmo.
-   O número de versão secundária do cliente é menor ou igual ao número de versão secundário do servidor.

É para seu benefício e os benefícios dos seus usuários para manter a compatibilidade com o versionsÂ, ou seja, modificar a interface para que apenas o número da versão secundária seja alterado. Você pode manter a compatibilidade com o sentido atual quando adiciona novos tipos de dados que não são usados por funções existentes e quando adiciona novas funções sem alterar a especificação da interface para funções existentes.

Altere o número de versão principal se qualquer uma das seguintes condições se aplicar:

-   Se você alterar um tipo de dados que é usado por uma função existente.
-   Se você alterar a especificação de interface para uma função existente (como adicionar ou remover um parâmetro).
-   Se você Adicionar retornos de chamada que são chamados por funções existentes.

Altere o número de versão secundária se todas as condições a seguir se aplicarem:

-   Se você adicionar definições de tipo ou constantes que não são usadas por nenhuma função ou retornos de chamada existentes.
-   Se você não alterar nenhuma função existente e adicionar novas funções à interface.
-   Se você Adicionar retornos de chamada que não são chamados por nenhuma função existente e os novos retornos de chamada seguirem quaisquer funções existentes.

Se suas modificações estiverem qualificadas como uma alteração compatível com o sentido da interface, use o procedimento a seguir.

**Para modificar o arquivo de interface (IDL)**

1.  Adicione novas definições de constantes e tipos ao arquivo de interface.
2.  Adicione funções de retorno de chamada ao final do arquivo de interface.
3.  Adicione novas funções ao final do arquivo de interface.

O atributo **\[ version \]** pode ocorrer no máximo uma vez no cabeçalho da interface.

Quando o atributo Version não estiver presente, a interface terá uma versão padrão de 0,0.

O caractere de período entre os números principal e secundário é um delimitador e não representa um ponto decimal. O número secundário é tratado como um inteiro. Os zeros à esquerda não são significativos. Os zeros à direita são significativos.

Por exemplo, a configuração de versão 1,11 representa um valor principal de um e um valor secundário de onze. A versão 1,11 não representa um valor entre 1,1 e 1,2.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**objeto**](object.md)
</dt> <dt>

[**personalizado**](uuid.md)
</dt> </dl>

 

 





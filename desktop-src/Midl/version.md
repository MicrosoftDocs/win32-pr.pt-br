---
title: atributo version
description: O atributo de interface \ version\ identifica uma versão específica entre várias versões de uma interface RPC. Com o atributo de versão, você garante que apenas as versões compatíveis do software cliente e servidor sejam permitidas para a vinculação.
ms.assetid: 66ac5cf3-2230-44fd-aaf6-8013e4a4ae81
keywords:
- atributo de versão MIDL
topic_type:
- apiref
api_name:
- version
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c72cc825183740d856c20b9e5c76ece472f82db405d9560e6502f6e32985b60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252106"
---
# <a name="version-attribute"></a>atributo version

O **\[ atributo \]** de interface de versão identifica uma versão específica entre várias versões de uma interface RPC. Com o atributo de versão, você garante que apenas as versões compatíveis do software cliente e servidor sejam permitidas para a vinculação.

``` syntax
version ( major-value[[. minor-value]] )
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor principal* 
</dt> <dd>

Especifica um inteiro sem sinal curto entre zero e 65.535, inclusive, que representa o número de versão principal.

</dd> <dt>

*valor secundário* 
</dt> <dd>

Especifica um inteiro sem sinal curto entre zero e 65.535, inclusive, que representa o número de versão secundária. O valor da versão secundária é opcional. Se estiver presente, o valor da versão secundária será separado do número de versão principal por um caractere de ponto (.). Se não for especificado, o valor da versão secundária será zero.

</dd> </dl>

## <a name="remarks"></a>Comentários

O compilador MIDL não dá suporte a várias versões de uma interface COM. Como resultado, uma lista de atributos de interface que inclui o atributo **\[** [**de**](object.md) **\]** objeto não pode incluir o atributo **\[ de \]** versão. Para criar uma nova versão de uma interface COM existente, use herança de interface. Uma interface COM derivada tem um UUID diferente, mas herda as funções membro da interface, códigos de status e atributos de interface da interface base.

Em combinação com o **\[** [**valor uuid,**](uuid.md) **\]** o **\[ valor \]** da versão identifica exclusivamente a interface. A biblioteca em tempo de executar passa **\[ os valores de \]** versão e **\[ uuid \]** para o servidor quando o cliente chama uma função remota. Um cliente pode se vincular a um servidor para uma determinada interface se:

-   O **\[ valor \] uuid** é o mesmo.
-   O número de versão principal é o mesmo.
-   O número de versão secundária do cliente é menor ou igual ao número de versão secundária do servidor.

É de seu benefício e do benefício dos usuários manter a compatibilidade ascendente entre as versões, ou seja, modificar a interface para que apenas o número de versão secundária seja modificado. Você pode manter a compatibilidade ascendente quando adiciona novos tipos de dados que não são usados por funções existentes e quando adiciona novas funções sem alterar a especificação da interface para funções existentes.

Altere o número de versão principal se qualquer uma das seguintes condições se aplicar:

-   Se você alterar um tipo de dados usado por uma função existente.
-   Se você alterar a especificação de interface de uma função existente (como adicionar ou remover um parâmetro).
-   Se você adicionar retornos de chamada que são chamados por funções existentes.

Altere o número de versão secundária se todas as seguintes condições se aplicarem:

-   Se você adicionar definições de tipo ou constantes que não são usadas por nenhuma função ou retornos de chamada existentes.
-   Se você não alterar nenhuma função existente e adicionar novas funções à interface.
-   Se você adicionar retornos de chamada que não são chamados por nenhuma função existente e os novos retornos de chamada seguirem as funções existentes.

Se suas modificações se qualificarem como uma alteração compatível para cima para a interface, use o procedimento a seguir.

**Para modificar o arquivo de interface (IDL)**

1.  Adicione novas definições de tipo e constante ao arquivo de interface.
2.  Adicione funções de retorno de chamada ao final do arquivo de interface.
3.  Adicione novas funções ao final do arquivo de interface.

O **\[ atributo \]** de versão pode ocorrer no máximo uma vez no header da interface.

Quando o atributo de versão não está presente, a interface tem uma versão padrão de 0.0.

O caractere de ponto entre os números principal e secundário é um secundário e não representa um ponto decimal. O número secundário é tratado como um inteiro. Zeros à esquerda não são significativos. Zeros à esquerda são significativos.

Por exemplo, a configuração de versão 1.11 representa um valor principal de um e um valor secundário de 11. A versão 1.11 não representa um valor entre 1.1 e 1.2.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**Interface**](interface.md)
</dt> <dt>

[**Objeto**](object.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> </dl>

 

 





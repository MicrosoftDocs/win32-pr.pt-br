---
title: atributo de importação
description: A diretiva de importação especifica outro arquivo IDL, ODL ou Header que contém as definições que você deseja referenciar do seu arquivo IDL principal.
ms.assetid: b52fb2c7-ce60-474f-8833-7a821844f747
keywords:
- importar atributo MIDL
topic_type:
- apiref
api_name:
- import
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff13c069c6bba819720a9d1120a42c25af4b51
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293937"
---
# <a name="import-attribute"></a>atributo de importação

A diretiva de **importação** especifica outro arquivo IDL, ODL ou Header que contém as definições que você deseja referenciar do seu arquivo IDL principal.

``` syntax
import "filename" [[ , ... ]] ;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome do arquivo* 
</dt> <dd>

Especifica o nome do arquivo de cabeçalho, IDL ou ODL a ser importado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Com a diretiva **Import** , todas as instruções IDL no arquivo importado, como TYPEDEFs, declarações de constantes e definições de interface, ficam disponíveis para a importação. Arquivo IDL.

O arquivo importado é processado separadamente (o que significa que o pré-processador de CPP é invocado de forma independente) do arquivo de importação de IDL. Dessa forma, as diretivas anteriores ao processador, como \# definir, não são transferidas de um cabeçalho ou arquivo IDL importado para o arquivo IDL de importação.

Assim como a macro de pré-processador de linguagem C, a diretiva de **importação** informa o compilador **\# para incluir tipos** de dados que foram definidos nos arquivos IDL importados. Ao contrário da diretiva **\# include** , a diretiva de **importação** ignora os protótipos de procedimento, pois nenhum stub é gerado para qualquer coisa no arquivo importado.

Para obter informações específicas sobre como usar a **importação** para incluir arquivos de cabeçalho em um arquivo IDL, consulte [Importando arquivos de cabeçalho do sistema](importing-system-header-files.md).

O cabeçalho do idioma C (. H) gerado para a interface não contém diretamente os tipos importados, mas, em vez disso, gera uma diretiva **\# include** para o arquivo de cabeçalho correspondente à interface importada. Por exemplo, quando você importa BASE. IDL em seu derivado. IDL, o arquivo de cabeçalho gerado derivado. H conterá a diretiva **\# include** base. H.

As seguintes regras se aplicam:

-   A palavra-chave de **importação** é opcional e pode aparecer zero ou mais vezes no arquivo IDL.
-   Cada palavra-chave de **importação** pode ser associada a mais de um nome de arquivo.
-   Separe vários nomes de arquivo com vírgulas.
-   Você deve colocar o nome do arquivo entre aspas e encerrar a instrução de importação com um ponto-e-vírgula (;).
-   Você pode importar uma interface que não tem atributos para outro arquivo IDL. No entanto, a interface deve conter apenas tipos de texto; Ele não pode conter nenhum procedimento. Se até um procedimento estiver contido na interface importada, você deverá especificar um atributo [**local**](local.md) ou [**UUID**](uuid.md) .
-   A função de **importação** é idempotentÂ â € ", ou seja, a importação de uma interface mais de uma vez não tem nenhum efeito adicional.

> [!Note]  
> O comportamento da diretiva de **importação** é independente do modo de compilador de MIDL alternar [**/MS \_ ext**](-ms-ext.md) (o padrão), [**/OSF**](-osf.md)e [**/app \_ config**](-app-config.md). No entanto, o modo de compilador (**/OSF** ou **/MS \_ ext**) pode afetar a decoração de atributo de ponteiro em tipos importados. Para obter detalhes [, consulte herança de tipo de atributo de ponteiro](/windows/desktop/Rpc/pointer-attribute-type-inheritance).

 

## <a name="examples"></a>Exemplos

``` syntax
import "myoldodl.odl";  
import "unknwn.idl";
import "part1.idl", "part2.idl", "part3.idl"; 
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**configuração do/App \_**](-app-config.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**incluir**](include.md)
</dt> <dt>

[Importar arquivos de cabeçalho do sistema](importing-system-header-files.md)
</dt> <dt>

[Importando arquivos e bibliotecas de tipos](importing-files-and-type-libraries.md)
</dt> <dt>

[**/MS \_ ext**](-ms-ext.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 
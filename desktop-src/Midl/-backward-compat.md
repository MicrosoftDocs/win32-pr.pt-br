---
title: Opção/backward_compat
description: A \_ opção compatível com/Backward direciona o compilador MIDL para desativar alguns recursos avançados ao gerar stubs RPC/com.
ms.assetid: eec0ade7-30a0-44e4-92e9-fb03ff657723
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69b558d01b33b99f7d1d9279f729b923ff58df0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105758422"
---
# <a name="backward_compat-switch"></a>\_opção compatível com/Backward

A \_ opção compatível com/Backward direciona o compilador MIDL para desativar alguns recursos avançados ao gerar stubs RPC/com.

``` syntax
midl /backward_compat { maybenull_sizeis | zeroout_alignmentgap | 
     BSTR_byvalue_escaping | string_defaultvalue | signed_wchar_t }
```

## <a name="switch-options"></a>Opções de comutação

*tamanho do maybenull \_*<dl> Aplica o atributo [ \[ desabilitar \_ \_ verificação \] de consistência](disable-consistence-check.md) a uma compilação de MIDL inteira.  
</dl>

*\_alignmentgapout zero*<dl> Desativa o zeramento de lacunas no buffer de marshaling.  
</dl>

*\_Saída de BYVALUE BSTR \_*<dl> Direciona o compilador MIDL para respeitar sequências de escape, como â € ̃ \\ NÂ €™ ou â € ̃ \\ tâ €™ em BSTRs.  
</dl>

*Cadeia de caracteres \_ DefaultValue*<dl> Força o compilador MIDL a forçar cadeias de caracteres em atributos [**\[ DEFAULTVALUE \]**](defaultvalue.md) em Variant. VT \_ i4 tipo antes de forçar o valor para o tipo correto.  
</dl>

*\_t de WCHAR assinado \_*<dl> Direciona MIDL para tratar o tipo WCHAR \_ t como assinado para compatibilidade com Visual Basic.  
</dl>

## <a name="remarks"></a>Comentários

-   *\_ tamanho do maybenull*: consulte \[ desabilitar \_ verificação de consistência \_ \] .
-   *\_ alignmentgapout de zeroout*: quando IDLs são compilados com â € "destino NT60 ou superior, o MIDL criará stubs que zeram quaisquer lacunas de alinhamento entre membros ou uma estrutura no buffer de conexão. A opção de linha de comando */Backward \_ compat zeroout \_ alignmentgap* direciona MIDL para desabilitar esse recurso.

    Na estrutura de exemplo a seguir, o buffer de conexão contém uma lacuna de alinhamento de 7 bytes para alinhar o membro do Hyper a 8 após o membro Char. Com â € "Target NT60 ou superior, MIDL zerará essa lacuna, a menos que a opção seja usada.

    Arquivo IDL:

    ``` syntax
    typedef struct _structwithgaps{
        char c;
        // 7 byte gap to align the following hyper to 8 
        hyper h;
    } structwithgap;
    ```

    Essa opção pode fornecer uma ligeira melhoria de desempenho com aumentos potencialmente significativos no risco de divulgação.

-   *\_ \_ Saída de ByValue de BSTR*: por padrão, o compilador MIDL não processa sequências de escape como â € ̃ \\ NÂ €™ ou â € ̃ \\ tâ €™ em constantes de cadeia de caracteres para automação OLE ao converter uma constante de cadeia de caracteres em tipos VT \_ LPSTR ou VT \_ LPWSTR. Com essa opção de opção de compatibilidade com versões anteriores, as sequências de escape são avaliadas.
-   *cadeia de caracteres \_ DefaultValue*: força o compilador MIDL a forçar cadeias numéricas em atributos [**\[ DefaultValue \]**](defaultvalue.md) em Variant. VT \_ i4 tipo antes de forçar o valor para o tipo correto. Isso pode levar à perda de precisão em alguns casos, portanto, essa opção de opção não é recomendada.
-   *\_ WCHAR \_ t assinado*: direciona MIDL para tratar o tipo WCHAR \_ t como assinado para compatibilidade com Visual Basic.

 

 





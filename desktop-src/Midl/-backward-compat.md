---
title: /backward_compat Switch
description: A opção de compatibilidade /backward direciona o compilador MIDL para desligar alguns recursos avançados ao gerar \_ stubs RPC/COM.
ms.assetid: eec0ade7-30a0-44e4-92e9-fb03ff657723
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd412bdabe4255a9a4538503b29ddf5681265ce5e16c81d3d5fc2484eb6c9675
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086386"
---
# <a name="backward_compat-switch"></a>/backward \_ compat Switch

A opção de compatibilidade /backward direciona o compilador MIDL para desligar alguns recursos avançados ao gerar \_ stubs RPC/COM.

``` syntax
midl /backward_compat { maybenull_sizeis | zeroout_alignmentgap | 
     BSTR_byvalue_escaping | string_defaultvalue | signed_wchar_t }
```

## <a name="switch-options"></a>Opções de opção

*maybenull \_ sizeis*<dl> Aplica o atributo [ \[ \_ desabilitar verificação \_ de consistência \] ](disable-consistence-check.md) a uma compilação MIDL inteira.  
</dl>

*alinhamento \_ zerooutgap*<dl> Desliga a zeração de lacunas no buffer com marshaling.  
</dl>

*Escape de \_ BSTR \_ byvalue*<dl> Direciona o compilador MIDL para manter sequências de escape, como â€ â€ ™ ou \\ â€ \\ tâ€™ em BSTRs.  
</dl>

*string \_ defaultvalue*<dl> Força o compilador MIDL a coerar cadeias de caracteres em [**\[ atributos defaultvalue \]**](defaultvalue.md) em VARIANT. Tipo \_ de VT I4 antes de coerção do valor no tipo correto.  
</dl>

*signed \_ wchar \_ t*<dl> Direciona MIDL para tratar o tipo wchar \_ t como assinado para compatibilidade com Visual Basic.  
</dl>

## <a name="remarks"></a>Comentários

-   *maybenull \_ sizeis:* consulte \[ desabilitar verificação \_ de \_ \] consistência.
-   alinhamento de *\_ zerooutgap:* quando as IDLs são compiladas com â€"target NT60 ou superior, o MIDL criará stubs que zeram as lacunas de alinhamento entre membros ou uma estrutura no buffer de transmissão. A opção de linha *de comando /backward \_ compat zeroout \_ alignmentgap* direciona MIDL para desabilitar esse recurso.

    Na estrutura de exemplo a seguir, o buffer de transmissão contém uma lacuna de alinhamento de 7 byte para alinhar o hiper membro a 8 após o membro char. Com o destino NT60 ou superior, MIDL zerará essa lacuna, a menos que a opção seja usada.

    Arquivo IDL:

    ``` syntax
    typedef struct _structwithgaps{
        char c;
        // 7 byte gap to align the following hyper to 8 
        hyper h;
    } structwithgap;
    ```

    Essa opção pode fornecer uma pequena melhoria de desempenho com aumentos potencialmente significativos no risco de divulgação.

-   Escape de *BSTR \_ byvalue: \_* por padrão, o compilador MIDL não processa sequências de escape, como â€ â€ ™ ou â€ tâ€™ em constantes de cadeia de caracteres para Automação OLE ao converter uma constante de cadeia de caracteres para tipos \\ VT LPSTR ou \\ \_ VT \_ LPWSTR. Com essa opção de opção de compatibilidade com compatibilidade com backward, as sequências de escape são avaliadas.
-   *string \_ defaultvalue:* força o compilador MIDL a coerar cadeias de caracteres numéricas em [**\[ atributos defaultvalue \]**](defaultvalue.md) em VARIANT. Tipo \_ de VT I4 antes de coerção do valor no tipo correto. Isso pode levar à perda de precisão em alguns casos, portanto, essa opção de opção não é recomendada.
-   *signed \_ wchar \_ t*: direciona MIDL para tratar o tipo wchar t como assinado para \_ compatibilidade com Visual Basic.

 

 





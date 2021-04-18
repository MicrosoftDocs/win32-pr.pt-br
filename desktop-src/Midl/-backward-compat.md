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
# <a name="backward_compat-switch"></a><span data-ttu-id="2dc03-103">\_opção compatível com/Backward</span><span class="sxs-lookup"><span data-stu-id="2dc03-103">/backward\_compat Switch</span></span>

<span data-ttu-id="2dc03-104">A \_ opção compatível com/Backward direciona o compilador MIDL para desativar alguns recursos avançados ao gerar stubs RPC/com.</span><span class="sxs-lookup"><span data-stu-id="2dc03-104">The /backward\_compat switch directs the MIDL compiler to turn off some advanced features when generating RPC/COM stubs.</span></span>

``` syntax
midl /backward_compat { maybenull_sizeis | zeroout_alignmentgap | 
     BSTR_byvalue_escaping | string_defaultvalue | signed_wchar_t }
```

## <a name="switch-options"></a><span data-ttu-id="2dc03-105">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="2dc03-105">Switch Options</span></span>

<span data-ttu-id="2dc03-106">*tamanho do maybenull \_*</span><span class="sxs-lookup"><span data-stu-id="2dc03-106">*maybenull\_sizeis*</span></span><dl> <span data-ttu-id="2dc03-107">Aplica o atributo [ \[ desabilitar \_ \_ verificação \] de consistência](disable-consistence-check.md) a uma compilação de MIDL inteira.</span><span class="sxs-lookup"><span data-stu-id="2dc03-107">Applies the [\[disable\_consistency\_check\]](disable-consistence-check.md) attribute to an entire MIDL compilation.</span></span>  
</dl>

<span data-ttu-id="2dc03-108">*\_alignmentgapout zero*</span><span class="sxs-lookup"><span data-stu-id="2dc03-108">*zeroout\_alignmentgap*</span></span><dl> <span data-ttu-id="2dc03-109">Desativa o zeramento de lacunas no buffer de marshaling.</span><span class="sxs-lookup"><span data-stu-id="2dc03-109">Turns off zeroing out gaps in the marshaled buffer.</span></span>  
</dl>

<span data-ttu-id="2dc03-110">*\_Saída de BYVALUE BSTR \_*</span><span class="sxs-lookup"><span data-stu-id="2dc03-110">*BSTR\_byvalue\_escaping*</span></span><dl> <span data-ttu-id="2dc03-111">Direciona o compilador MIDL para respeitar sequências de escape, como â € ̃ \\ NÂ €™ ou â € ̃ \\ tâ €™ em BSTRs.</span><span class="sxs-lookup"><span data-stu-id="2dc03-111">Directs the MIDL compiler to honor escape sequences such as â€˜\\nâ€™ or â€˜\\tâ€™ in BSTRs.</span></span>  
</dl>

<span data-ttu-id="2dc03-112">*Cadeia de caracteres \_ DefaultValue*</span><span class="sxs-lookup"><span data-stu-id="2dc03-112">*string\_defaultvalue*</span></span><dl> <span data-ttu-id="2dc03-113">Força o compilador MIDL a forçar cadeias de caracteres em atributos [**\[ DEFAULTVALUE \]**](defaultvalue.md) em Variant. VT \_ i4 tipo antes de forçar o valor para o tipo correto.</span><span class="sxs-lookup"><span data-stu-id="2dc03-113">Forces the MIDL compiler to coerce strings in [**\[defaultvalue\]**](defaultvalue.md) attributes into VARIANT.VT\_I4 type before coercing the value into the correct type.</span></span>  
</dl>

<span data-ttu-id="2dc03-114">*\_t de WCHAR assinado \_*</span><span class="sxs-lookup"><span data-stu-id="2dc03-114">*signed\_wchar\_t*</span></span><dl> <span data-ttu-id="2dc03-115">Direciona MIDL para tratar o tipo WCHAR \_ t como assinado para compatibilidade com Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2dc03-115">Directs MIDL to treat the wchar\_t type as signed for compatibility with Visual Basic.</span></span>  
</dl>

## <a name="remarks"></a><span data-ttu-id="2dc03-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2dc03-116">Remarks</span></span>

-   <span data-ttu-id="2dc03-117">*\_ tamanho do maybenull*: consulte \[ desabilitar \_ verificação de consistência \_ \] .</span><span class="sxs-lookup"><span data-stu-id="2dc03-117">*maybenull\_sizeis*: See \[disable\_consistency\_check\].</span></span>
-   <span data-ttu-id="2dc03-118">*\_ alignmentgapout de zeroout*: quando IDLs são compilados com â € "destino NT60 ou superior, o MIDL criará stubs que zeram quaisquer lacunas de alinhamento entre membros ou uma estrutura no buffer de conexão.</span><span class="sxs-lookup"><span data-stu-id="2dc03-118">*zeroout\_alignmentgap*: When IDLs are compiled with â€“target NT60 or higher, MIDL will create stubs that zero out any alignment gaps between members or a structure in the wire buffer.</span></span> <span data-ttu-id="2dc03-119">A opção de linha de comando */Backward \_ compat zeroout \_ alignmentgap* direciona MIDL para desabilitar esse recurso.</span><span class="sxs-lookup"><span data-stu-id="2dc03-119">The command line switch */backward\_compat zeroout\_alignmentgap* directs MIDL to disable this feature.</span></span>

    <span data-ttu-id="2dc03-120">Na estrutura de exemplo a seguir, o buffer de conexão contém uma lacuna de alinhamento de 7 bytes para alinhar o membro do Hyper a 8 após o membro Char.</span><span class="sxs-lookup"><span data-stu-id="2dc03-120">In the following example structure, the wire buffer contains a 7 byte alignment gap to align the hyper member to 8 after the char member.</span></span> <span data-ttu-id="2dc03-121">Com â € "Target NT60 ou superior, MIDL zerará essa lacuna, a menos que a opção seja usada.</span><span class="sxs-lookup"><span data-stu-id="2dc03-121">With â€“target NT60 or higher, MIDL will zero out that gap unless the switch is used.</span></span>

    <span data-ttu-id="2dc03-122">Arquivo IDL:</span><span class="sxs-lookup"><span data-stu-id="2dc03-122">IDL file:</span></span>

    ``` syntax
    typedef struct _structwithgaps{
        char c;
        // 7 byte gap to align the following hyper to 8 
        hyper h;
    } structwithgap;
    ```

    <span data-ttu-id="2dc03-123">Essa opção pode fornecer uma ligeira melhoria de desempenho com aumentos potencialmente significativos no risco de divulgação.</span><span class="sxs-lookup"><span data-stu-id="2dc03-123">This switch can provide a slight performance improvement with potentially significant increases in disclosure risk.</span></span>

-   <span data-ttu-id="2dc03-124">*\_ \_ Saída de ByValue de BSTR*: por padrão, o compilador MIDL não processa sequências de escape como â € ̃ \\ NÂ €™ ou â € ̃ \\ tâ €™ em constantes de cadeia de caracteres para automação OLE ao converter uma constante de cadeia de caracteres em tipos VT \_ LPSTR ou VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="2dc03-124">*BSTR\_byvalue\_escaping*: By default, the MIDL compiler does not process escape sequences such as â€˜\\nâ€™ or â€˜\\tâ€™ in string constants for OLE Automation when converting a string constant to types VT\_LPSTR or VT\_LPWSTR.</span></span> <span data-ttu-id="2dc03-125">Com essa opção de opção de compatibilidade com versões anteriores, as sequências de escape são avaliadas.</span><span class="sxs-lookup"><span data-stu-id="2dc03-125">With this backward compatibility switch option, the escape sequences are evaluated.</span></span>
-   <span data-ttu-id="2dc03-126">*cadeia de caracteres \_ DefaultValue*: força o compilador MIDL a forçar cadeias numéricas em atributos [**\[ DefaultValue \]**](defaultvalue.md) em Variant. VT \_ i4 tipo antes de forçar o valor para o tipo correto.</span><span class="sxs-lookup"><span data-stu-id="2dc03-126">*string\_defaultvalue*: Forces the MIDL compiler to coerce numeric strings in [**\[defaultvalue\]**](defaultvalue.md) attributes into VARIANT.VT\_I4 type before coercing the value into the correct type.</span></span> <span data-ttu-id="2dc03-127">Isso pode levar à perda de precisão em alguns casos, portanto, essa opção de opção não é recomendada.</span><span class="sxs-lookup"><span data-stu-id="2dc03-127">This can lead to loss of precision in some cases, so this switch option is not recommended.</span></span>
-   <span data-ttu-id="2dc03-128">*\_ WCHAR \_ t assinado*: direciona MIDL para tratar o tipo WCHAR \_ t como assinado para compatibilidade com Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2dc03-128">*signed\_wchar\_t*: Directs MIDL to treat the wchar\_t type as signed for compatibility with Visual Basic.</span></span>

 

 





---
title: Recurso de ACELERAdores
description: Define um ou mais aceleradores para um aplicativo. Um acelerador é um pressionamento de tecla definido pelo aplicativo para fornecer ao usuário uma maneira rápida de executar uma tarefa.
ms.assetid: 5953ee2d-b7a7-45d2-8445-4cba1207e272
keywords:
- Menus de recursos de ACELERAdores e outros recursos
topic_type:
- apiref
api_name:
- ACCELERATORS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aeb09ca52438f7b2f4903e5403eeb722e5d7d7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104499032"
---
# <a name="accelerators-resource"></a><span data-ttu-id="b1111-105">Recurso de ACELERAdores</span><span class="sxs-lookup"><span data-stu-id="b1111-105">ACCELERATORS resource</span></span>

<span data-ttu-id="b1111-106">Define um ou mais aceleradores para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b1111-106">Defines one or more accelerators for an application.</span></span> <span data-ttu-id="b1111-107">Um acelerador é um pressionamento de tecla definido pelo aplicativo para fornecer ao usuário uma maneira rápida de executar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="b1111-107">An accelerator is a keystroke defined by the application to give the user a quick way to perform a task.</span></span>

``` syntax
acctablename ACCELERATORS [optional-statements] {event, idvalue, [type] [options]... }
```

## <a name="parameters"></a><span data-ttu-id="b1111-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1111-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1111-109"><span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*</span><span class="sxs-lookup"><span data-stu-id="b1111-109"><span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*</span></span>
</dt> <dd>

<span data-ttu-id="b1111-110">Nome exclusivo ou um valor inteiro sem sinal de 16 bits que identifica o recurso.</span><span class="sxs-lookup"><span data-stu-id="b1111-110">Unique name or a 16-bit unsigned integer value that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="b1111-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instruções opcionais*</span><span class="sxs-lookup"><span data-stu-id="b1111-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="b1111-112">Zero ou mais das instruções a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1111-112">Zero or more of the following statements.</span></span>



| <span data-ttu-id="b1111-113">Instrução</span><span class="sxs-lookup"><span data-stu-id="b1111-113">Statement</span></span>                                                        | <span data-ttu-id="b1111-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1111-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1111-115">[**Características**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="b1111-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="b1111-116">Informações definidas pelo usuário sobre um recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="b1111-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="b1111-117">Para obter mais informações, consulte [**características**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b1111-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="b1111-118">[](language-statement.md) *Idioma* do idioma, *subidioma*</span><span class="sxs-lookup"><span data-stu-id="b1111-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="b1111-119">Especifica o idioma do recurso.</span><span class="sxs-lookup"><span data-stu-id="b1111-119">Specifies the language for the resource.</span></span> <span data-ttu-id="b1111-120">Para obter mais informações, consulte [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b1111-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                              |
| <span data-ttu-id="b1111-121">[](version-statement.md) *DWORD* da versão</span><span class="sxs-lookup"><span data-stu-id="b1111-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="b1111-122">Número de versão definido pelo usuário para o recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="b1111-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="b1111-123">Para obter mais informações, consulte [**versão**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b1111-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="b1111-124"><span id="event"></span><span id="EVENT"></span>*circunstância*</span><span class="sxs-lookup"><span data-stu-id="b1111-124"><span id="event"></span><span id="EVENT"></span>*event*</span></span>
</dt> <dd>

<span data-ttu-id="b1111-125">Tecla a ser usada como um acelerador.</span><span class="sxs-lookup"><span data-stu-id="b1111-125">Keystroke to be used as an accelerator.</span></span> <span data-ttu-id="b1111-126">Pode ser qualquer um dos tipos de caracteres a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1111-126">It can be any one of the following character types.</span></span>



| <span data-ttu-id="b1111-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1111-127">Type</span></span>                    | <span data-ttu-id="b1111-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1111-128">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1111-129">"*Char*"</span><span class="sxs-lookup"><span data-stu-id="b1111-129">"*char*"</span></span>                | <span data-ttu-id="b1111-130">Um único caractere entre aspas duplas (").</span><span class="sxs-lookup"><span data-stu-id="b1111-130">A single character enclosed in double quotation marks (").</span></span> <span data-ttu-id="b1111-131">O caractere pode ser precedido por um acento circunflexo (^), o que significa que o caractere é um caractere de controle.</span><span class="sxs-lookup"><span data-stu-id="b1111-131">The character can be preceded by a caret (^), meaning that the character is a control character.</span></span>                                                                                  |
| <span data-ttu-id="b1111-132">*Caractere*</span><span class="sxs-lookup"><span data-stu-id="b1111-132">*Character*</span></span>             | <span data-ttu-id="b1111-133">Um valor inteiro que representa um caractere.</span><span class="sxs-lookup"><span data-stu-id="b1111-133">An integer value representing a character.</span></span> <span data-ttu-id="b1111-134">O parâmetro de *tipo* deve ser **ASCII**.</span><span class="sxs-lookup"><span data-stu-id="b1111-134">The *type* parameter must be **ASCII**.</span></span>                                                                                                                                                           |
| <span data-ttu-id="b1111-135">*caractere de chave virtual*</span><span class="sxs-lookup"><span data-stu-id="b1111-135">*virtual-key character*</span></span> | <span data-ttu-id="b1111-136">Um valor inteiro que representa uma chave virtual.</span><span class="sxs-lookup"><span data-stu-id="b1111-136">An integer value representing a virtual key.</span></span> <span data-ttu-id="b1111-137">A chave virtual para chaves alfanuméricas pode ser especificada colocando-se a letra maiúscula ou o número entre aspas duplas (por exemplo, "9" ou "C").</span><span class="sxs-lookup"><span data-stu-id="b1111-137">The virtual key for alphanumeric keys can be specified by placing the uppercase letter or number in double quotation marks (for example, "9" or "C").</span></span> <span data-ttu-id="b1111-138">O parâmetro de *tipo* deve ser **VIRTKEY**.</span><span class="sxs-lookup"><span data-stu-id="b1111-138">The *type* parameter must be **VIRTKEY**.</span></span> |



 

</dd> <dt>

<span data-ttu-id="b1111-139"><span id="idvalue"></span><span id="IDVALUE"></span>*idvalue*</span><span class="sxs-lookup"><span data-stu-id="b1111-139"><span id="idvalue"></span><span id="IDVALUE"></span>*idvalue*</span></span>
</dt> <dd>

<span data-ttu-id="b1111-140">um valor inteiro sem sinal de 16 bits que identifica o acelerador.</span><span class="sxs-lookup"><span data-stu-id="b1111-140">a 16-bit unsigned integer value that identifies the accelerator.</span></span>

</dd> <dt>

<span data-ttu-id="b1111-141"><span id="type"></span><span id="TYPE"></span>*Escreva*</span><span class="sxs-lookup"><span data-stu-id="b1111-141"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="b1111-142">Necessário somente quando o parâmetro de *evento* é um *caractere ou um* caractere de *chave virtual*.</span><span class="sxs-lookup"><span data-stu-id="b1111-142">Required only when the *event* parameter is a *character* or a *virtual-key character*.</span></span> <span data-ttu-id="b1111-143">O parâmetro de *tipo* especifica **ASCII** ou **VIRTKEY**; o valor inteiro do *evento* é interpretado de acordo.</span><span class="sxs-lookup"><span data-stu-id="b1111-143">The *type* parameter specifies either **ASCII** or **VIRTKEY**; the integer value of *event* is interpreted accordingly.</span></span> <span data-ttu-id="b1111-144">Quando **VIRTKEY** é especificado e o *evento* contém uma cadeia de caracteres, o *evento* deve estar em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="b1111-144">When **VIRTKEY** is specified and *event* contains a string, *event* must be uppercase.</span></span>

</dd> <dt>

<span data-ttu-id="b1111-145"><span id="options"></span><span id="OPTIONS"></span>*Opções*</span><span class="sxs-lookup"><span data-stu-id="b1111-145"><span id="options"></span><span id="OPTIONS"></span>*options*</span></span>
</dt> <dd>

<span data-ttu-id="b1111-146">opções que definem o acelerador.</span><span class="sxs-lookup"><span data-stu-id="b1111-146">options that define the accelerator.</span></span> <span data-ttu-id="b1111-147">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1111-147">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="b1111-148">Opção</span><span class="sxs-lookup"><span data-stu-id="b1111-148">Option</span></span>                             | <span data-ttu-id="b1111-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1111-149">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1111-150">**Inverter**</span><span class="sxs-lookup"><span data-stu-id="b1111-150">**NOINVERT**</span></span>                       | <span data-ttu-id="b1111-151">Especifica que nenhum item de menu de nível superior é realçado quando o acelerador é usado.</span><span class="sxs-lookup"><span data-stu-id="b1111-151">Specifies that no top-level menu item is highlighted when the accelerator is used.</span></span> <span data-ttu-id="b1111-152">Isso é útil ao definir aceleradores para ações como rolagem que não correspondem a um item de menu.</span><span class="sxs-lookup"><span data-stu-id="b1111-152">This is useful when defining accelerators for actions such as scrolling that do not correspond to a menu item.</span></span> <span data-ttu-id="b1111-153">Se **Invert** for omitido, um item de menu de nível superior será realçado (se possível) quando o acelerador for usado.</span><span class="sxs-lookup"><span data-stu-id="b1111-153">If **NOINVERT** is omitted, a top-level menu item will be highlighted (if possible) when the accelerator is used.</span></span> <span data-ttu-id="b1111-154">Este atributo é obsoleto e mantido somente para compatibilidade com versões anteriores com arquivos de recursos projetados para o Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b1111-154">This attribute is obsolete and retained only for backward compatibility with resource files designed for 16-bit Windows.</span></span> |
| <span data-ttu-id="b1111-155">**ALT**</span><span class="sxs-lookup"><span data-stu-id="b1111-155">**ALT**</span></span>                            | <span data-ttu-id="b1111-156">Faz com que o acelerador seja ativado somente se a tecla ALT estiver inativa.</span><span class="sxs-lookup"><span data-stu-id="b1111-156">Causes the accelerator to be activated only if the ALT key is down.</span></span> <span data-ttu-id="b1111-157">Aplica-se somente a chaves virtuais.</span><span class="sxs-lookup"><span data-stu-id="b1111-157">Applies only to virtual keys.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="b1111-158">**ALTERNÂNCIA**</span><span class="sxs-lookup"><span data-stu-id="b1111-158">**SHIFT**</span></span>                          | <span data-ttu-id="b1111-159">Faz com que o acelerador seja ativado somente se a tecla SHIFT estiver inativa.</span><span class="sxs-lookup"><span data-stu-id="b1111-159">Causes the accelerator to be activated only if the SHIFT key is down.</span></span> <span data-ttu-id="b1111-160">Aplica-se somente a chaves virtuais</span><span class="sxs-lookup"><span data-stu-id="b1111-160">Applies only to virtual keys</span></span>                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="b1111-161">**CONTROLO**</span><span class="sxs-lookup"><span data-stu-id="b1111-161">**CONTROL**</span></span>](control-control.md) | <span data-ttu-id="b1111-162">Define o caractere como um caractere de controle (o acelerador só será ativado se a tecla de controle estiver inoperante).</span><span class="sxs-lookup"><span data-stu-id="b1111-162">Defines the character as a control character (the accelerator is only activated if the CONTROL key is down).</span></span> <span data-ttu-id="b1111-163">Isso tem o mesmo efeito que usar um acento circunflexo (^) antes do caractere de acelerador no parâmetro de *evento* .</span><span class="sxs-lookup"><span data-stu-id="b1111-163">This has the same effect as using a caret (^) before the accelerator character in the *event* parameter.</span></span> <span data-ttu-id="b1111-164">Aplica-se somente a chaves virtuais</span><span class="sxs-lookup"><span data-stu-id="b1111-164">Applies only to virtual keys</span></span>                                                                                                                                                                                           |



 

</dd> </dl>

<span data-ttu-id="b1111-165">Alguns atributos também têm suporte para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="b1111-165">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="b1111-166">Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="b1111-166">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b1111-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1111-167">Remarks</span></span>

<span data-ttu-id="b1111-168">A função [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) é usada para converter mensagens do acelerador da fila do aplicativo no [**\_ comando do WM**](./wm-command.md) ou em mensagens [**\_ SYSCOMMAND do WM**](./wm-syscommand.md) .</span><span class="sxs-lookup"><span data-stu-id="b1111-168">The [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) function is used to translate accelerator messages from the application queue into [**WM\_COMMAND**](./wm-command.md) or [**WM\_SYSCOMMAND**](./wm-syscommand.md) messages.</span></span>

## <a name="examples"></a><span data-ttu-id="b1111-169">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b1111-169">Examples</span></span>

<span data-ttu-id="b1111-170">O exemplo a seguir demonstra o uso de teclas de aceleração.</span><span class="sxs-lookup"><span data-stu-id="b1111-170">The following example demonstrates the use of accelerator keys.</span></span>

``` syntax
1 ACCELERATORS
{
  "^C",  IDDCLEAR         ; control C
  "K",   IDDCLEAR         ; shift K
  "k",   IDDELLIPSE, ALT  ; alt k
  98,    IDDRECT, ASCII   ; b
  66,    IDDSTAR, ASCII   ; B (shift b)
  "g",   IDDRECT          ; g
  "G",   IDDSTAR          ; G (shift G)
  VK_F1, IDDCLEAR, VIRTKEY                ; F1
  VK_F1, IDDSTAR, CONTROL, VIRTKEY        ; control F1
  VK_F1, IDDELLIPSE, SHIFT, VIRTKEY       ; shift F1
  VK_F1, IDDRECT, ALT, VIRTKEY            ; alt F1
  VK_F2, IDDCLEAR, ALT, SHIFT, VIRTKEY    ; alt shift F2
  VK_F2, IDDSTAR, CONTROL, SHIFT, VIRTKEY ; ctrl shift F2
  VK_F2, IDDRECT, ALT, CONTROL, VIRTKEY   ; alt control F2
}
```

## <a name="see-also"></a><span data-ttu-id="b1111-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1111-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1111-172">Usando aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="b1111-172">Using Keyboard Accelerators</span></span>](./using-keyboard-accelerators.md)
</dt> <dt>

[<span data-ttu-id="b1111-173">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="b1111-173">**TranslateAccelerator**</span></span>](/windows/win32/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="b1111-174">**CARACTERÍSTICAS**</span><span class="sxs-lookup"><span data-stu-id="b1111-174">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="b1111-175">**'**</span><span class="sxs-lookup"><span data-stu-id="b1111-175">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="b1111-176">**IDIOMA**</span><span class="sxs-lookup"><span data-stu-id="b1111-176">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="b1111-177">**ADICIONARMENU**</span><span class="sxs-lookup"><span data-stu-id="b1111-177">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="b1111-178">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="b1111-178">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="b1111-179">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="b1111-179">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="b1111-180">**Versão**</span><span class="sxs-lookup"><span data-stu-id="b1111-180">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
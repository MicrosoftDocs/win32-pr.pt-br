---
title: Suporte à localização para controles comuns
description: Este tópico descreve o suporte para idiomas nacionais que são incorporados aos controles comuns.
ms.assetid: c5720198-9071-4213-8dad-50b4c015c5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ccc307defa687c8640425dd781660641fe78a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916065"
---
# <a name="localization-support-for-common-controls"></a><span data-ttu-id="b51a3-103">Suporte à localização para controles comuns</span><span class="sxs-lookup"><span data-stu-id="b51a3-103">Localization Support for Common Controls</span></span>

<span data-ttu-id="b51a3-104">Este tópico descreve o suporte para idiomas nacionais que são incorporados aos controles comuns.</span><span class="sxs-lookup"><span data-stu-id="b51a3-104">This topic describes the support for national languages that is built into the common controls.</span></span> <span data-ttu-id="b51a3-105">O suporte ao idioma nacional interno simplifica a implementação de aplicativos localizados.</span><span class="sxs-lookup"><span data-stu-id="b51a3-105">The built-in national language support simplifies the implementation of localized applications.</span></span>

<span data-ttu-id="b51a3-106">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="b51a3-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="b51a3-107">Especificando um idioma para os controles comuns</span><span class="sxs-lookup"><span data-stu-id="b51a3-107">Specifying a Language for the Common Controls</span></span>](#specifying-a-language-for-the-common-controls)
-   [<span data-ttu-id="b51a3-108">Especificando um idioma para controles em uma caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="b51a3-108">Specifying a Language for Controls in a Dialog Box</span></span>](#specifying-a-language-for-controls-in-a-dialog-box)
-   [<span data-ttu-id="b51a3-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b51a3-109">Related topics</span></span>](#related-topics)

## <a name="specifying-a-language-for-the-common-controls"></a><span data-ttu-id="b51a3-110">Especificando um idioma para os controles comuns</span><span class="sxs-lookup"><span data-stu-id="b51a3-110">Specifying a Language for the Common Controls</span></span>

<span data-ttu-id="b51a3-111">Se você quiser especificar um idioma para os controles comuns que seja diferente do idioma do sistema, chame [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span><span class="sxs-lookup"><span data-stu-id="b51a3-111">If you want to specify a language for the common controls that is different than the system language, call [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span></span> <span data-ttu-id="b51a3-112">O idioma especificado por essa função se aplica somente ao processo do qual a função é chamada.</span><span class="sxs-lookup"><span data-stu-id="b51a3-112">The language specified by this function applies only to the process from which the function is called.</span></span>

<span data-ttu-id="b51a3-113">Para determinar o idioma que está sendo usado atualmente pelos controles comuns, chame [**GetMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage).</span><span class="sxs-lookup"><span data-stu-id="b51a3-113">To determine the language currently being used by the common controls, call [**GetMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage).</span></span> <span data-ttu-id="b51a3-114">Ele retorna o valor que foi definido por uma chamada anterior para [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span><span class="sxs-lookup"><span data-stu-id="b51a3-114">It returns the value that was set by a previous call to [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span></span> <span data-ttu-id="b51a3-115">O idioma retornado é aquele que foi especificado para o processo do qual ele é chamado.</span><span class="sxs-lookup"><span data-stu-id="b51a3-115">The language returned is the one that was specified for the process it is called from.</span></span> <span data-ttu-id="b51a3-116">Se **InitMUILanguage** não tiver sido chamado ou for chamado de outro processo, **GetMUILanguage** retornará um valor padrão.</span><span class="sxs-lookup"><span data-stu-id="b51a3-116">If **InitMUILanguage** has not been called, or was called from another process, **GetMUILanguage** will return a default value.</span></span>

## <a name="specifying-a-language-for-controls-in-a-dialog-box"></a><span data-ttu-id="b51a3-117">Especificando um idioma para controles em uma caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="b51a3-117">Specifying a Language for Controls in a Dialog Box</span></span>

<span data-ttu-id="b51a3-118">Ao contrário dos controles comuns, os controles predefinidos, como botões ou caixas de edição, não usam o idioma do sistema atual por padrão.</span><span class="sxs-lookup"><span data-stu-id="b51a3-118">Unlike common controls, predefined controls such as buttons or edit boxes do not use the current system language by default.</span></span> <span data-ttu-id="b51a3-119">O controle de fonte nativo é um controle invisível que funciona em segundo plano para permitir que os controles predefinidos de uma caixa de diálogo exibam o idioma atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="b51a3-119">The native font control is an invisible control that works in the background to allow a dialog box's predefined controls to display the current system language.</span></span>

<span data-ttu-id="b51a3-120">Para usar o controle de fonte nativo, siga este procedimento.</span><span class="sxs-lookup"><span data-stu-id="b51a3-120">To use the native font control, follow this procedure.</span></span>

1.  <span data-ttu-id="b51a3-121">Inicialize o controle de fonte nativo chamando [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span><span class="sxs-lookup"><span data-stu-id="b51a3-121">Initialize the native font control by calling [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span></span> <span data-ttu-id="b51a3-122">Defina o membro **dwICC** da estrutura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) apontada por *LPINITCTRLS* para a \_ classe NATIVEFNTCTL ICC \_ .</span><span class="sxs-lookup"><span data-stu-id="b51a3-122">Set the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure pointed to by *lpInitCtrls* to ICC\_NATIVEFNTCTL\_CLASS.</span></span>
2.  <span data-ttu-id="b51a3-123">Adicione o controle ao script de recurso para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b51a3-123">Add the control to the resource script for the dialog box.</span></span> <span data-ttu-id="b51a3-124">Defina um ou mais dos seguintes sinalizadores de estilo para especificar quais controles serão afetados.</span><span class="sxs-lookup"><span data-stu-id="b51a3-124">Set one or more of the following style flags to specify which controls will be affected.</span></span> 

    | <span data-ttu-id="b51a3-125">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="b51a3-125">Flag</span></span>              | <span data-ttu-id="b51a3-126">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="b51a3-126">Applies to</span></span>                                                                                                                                                                                                                                                       |
    |-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="b51a3-127">edição de NFS \_</span><span class="sxs-lookup"><span data-stu-id="b51a3-127">NFS\_EDIT</span></span>         | <span data-ttu-id="b51a3-128">Editar controles</span><span class="sxs-lookup"><span data-stu-id="b51a3-128">Edit controls</span></span>                                                                                                                                                                                                                                                    |
    | <span data-ttu-id="b51a3-129">NFS \_ estático</span><span class="sxs-lookup"><span data-stu-id="b51a3-129">NFS\_STATIC</span></span>       | <span data-ttu-id="b51a3-130">Controles estáticos</span><span class="sxs-lookup"><span data-stu-id="b51a3-130">Static controls</span></span>                                                                                                                                                                                                                                                  |
    | <span data-ttu-id="b51a3-131">\_LISTCOMBO NFS</span><span class="sxs-lookup"><span data-stu-id="b51a3-131">NFS\_LISTCOMBO</span></span>    | <span data-ttu-id="b51a3-132">Controles List, ComboBox, List-View e ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="b51a3-132">List, ComboBox, List-View, and ComboBoxEx controls</span></span>                                                                                                                                                                                                               |
    | <span data-ttu-id="b51a3-133">\_botão NFS</span><span class="sxs-lookup"><span data-stu-id="b51a3-133">NFS\_BUTTON</span></span>       | <span data-ttu-id="b51a3-134">Controles de botão</span><span class="sxs-lookup"><span data-stu-id="b51a3-134">Button controls</span></span>                                                                                                                                                                                                                                                  |
    | <span data-ttu-id="b51a3-135">\_todos os NFS</span><span class="sxs-lookup"><span data-stu-id="b51a3-135">NFS\_ALL</span></span>          | <span data-ttu-id="b51a3-136">Todos os controles</span><span class="sxs-lookup"><span data-stu-id="b51a3-136">All controls</span></span>                                                                                                                                                                                                                                                     |
    | <span data-ttu-id="b51a3-137">\_USEFONTASSOC NFS</span><span class="sxs-lookup"><span data-stu-id="b51a3-137">NFS\_USEFONTASSOC</span></span> | <span data-ttu-id="b51a3-138">Plataforma leste asiático.</span><span class="sxs-lookup"><span data-stu-id="b51a3-138">East Asian platform.</span></span> <span data-ttu-id="b51a3-139">O controle usa o recurso de associação de fonte em vez de alternar para a fonte nativa.</span><span class="sxs-lookup"><span data-stu-id="b51a3-139">The control uses the font association feature instead of switching to the native font.</span></span> <span data-ttu-id="b51a3-140">Todas as outras plataformas a ignoram.</span><span class="sxs-lookup"><span data-stu-id="b51a3-140">All other platforms ignore it.</span></span> <span data-ttu-id="b51a3-141">Isso foi preterido para o Windows Vista e não tem suporte no COMCTL v6.</span><span class="sxs-lookup"><span data-stu-id="b51a3-141">This is deprecated for Windows Vista, and is not supported in comctl v6.</span></span> <span data-ttu-id="b51a3-142">Isso existe no COMCTL v5 por motivos herdados.</span><span class="sxs-lookup"><span data-stu-id="b51a3-142">This exists in comctl v5 for legacy reasons.</span></span> |

    

     

<span data-ttu-id="b51a3-143">O exemplo a seguir ilustra como adicionar um controle de fonte nativo a um script de recurso.</span><span class="sxs-lookup"><span data-stu-id="b51a3-143">The following example illustrates how to add a native font control to a resource script.</span></span> <span data-ttu-id="b51a3-144">Isso faz com que os controles de edição, lista e combinação da caixa de diálogo exibam texto usando o idioma atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="b51a3-144">It causes the dialog box's edit, list, and combo box controls to display text using the current system language.</span></span>


```
CONTROL    "",-1,"NativeFontCtl",NFS_EDIT|NFS_LISTCOMBO,0,0,0,0
```



## <a name="related-topics"></a><span data-ttu-id="b51a3-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b51a3-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b51a3-146">Sobre controles comuns</span><span class="sxs-lookup"><span data-stu-id="b51a3-146">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 





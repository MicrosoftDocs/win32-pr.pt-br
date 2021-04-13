---
title: Informações do registro de controles ActiveX
description: Informações do registro de controles ActiveX
ms.assetid: fda5b1e6-2048-4df7-ba8f-145652e3883c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b180b327a4239b220185a9073ebc7bc0826c39
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104499161"
---
# <a name="activex-controls-registry-information"></a><span data-ttu-id="22ff6-103">Informações do registro de controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="22ff6-103">ActiveX Controls Registry Information</span></span>

<span data-ttu-id="22ff6-104">Há várias entradas de registro e sinalizadores que são usados.</span><span class="sxs-lookup"><span data-stu-id="22ff6-104">There are a number of registry entries and flags that are used.</span></span> <span data-ttu-id="22ff6-105">Além disso, os controles podem dar suporte a categorias de componentes para classificar os recursos que eles fornecem.</span><span class="sxs-lookup"><span data-stu-id="22ff6-105">Additionally, controls can support component categories to classify the features they provide.</span></span>

<span data-ttu-id="22ff6-106">As chaves do registro relacionadas aos controles são marcadas com um asterisco na seguinte árvore:</span><span class="sxs-lookup"><span data-stu-id="22ff6-106">Registry keys related to controls are marked with an asterisk in the following tree:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {control_CLSID}
         ProgID = <identifier>
         InprocServer32 = <filename>.dll
         *DefaultIcon = <filename>.<ext>,resourceID
         *ToolboxBitmap32 = <filename>.<ext>,resourceID
         *Control
         verb
            *n = &Properties...
         *MiscStatus = 0
         TypeLib = {object_typelibID}
         *Version = version_number
```

<span data-ttu-id="22ff6-107">A entrada **DefaultIcon** é usada para identificar um ícone a ser exibido quando o controle é minimizado para um ícone.</span><span class="sxs-lookup"><span data-stu-id="22ff6-107">The **DefaultIcon** entry is used to identify an icon to be displayed when the control is minimized to an icon.</span></span> <span data-ttu-id="22ff6-108">A função [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona) é usada para obter o ícone do. DLL ou. Arquivo EXE especificado.</span><span class="sxs-lookup"><span data-stu-id="22ff6-108">The [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona) function is used to get the icon from the .DLL or .EXE file specified.</span></span>

<span data-ttu-id="22ff6-109">A entrada **ToolboxBitmap32** identifica o nome do módulo e o identificador de recurso para um bitmap de 16 \* 15 a ser usado para a face de uma barra de ferramentas ou botão de caixa de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="22ff6-109">The **ToolboxBitmap32** entry identifies the module name and resource identifier for a 16\*15 bitmap to use for the face of a toolbar or toolbox button.</span></span> <span data-ttu-id="22ff6-110">O tamanho do ícone padrão do Windows é muito grande para ser usado para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="22ff6-110">The standard Windows icon size is too large to be used for this purpose.</span></span> <span data-ttu-id="22ff6-111">Essa entrada especificamente dá suporte a contêineres de controle que têm um modo de design no qual um seleciona os controles e os coloca em um formulário que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="22ff6-111">This entry specifically supports control containers that have a design mode in which one selects controls and places them on a form being designed.</span></span> <span data-ttu-id="22ff6-112">Por exemplo, em Visual Basic, o ícone do controle é exibido na caixa de ferramentas Visual Basic durante o modo de design.</span><span class="sxs-lookup"><span data-stu-id="22ff6-112">For example, in Visual Basic, the control's icon is displayed in the Visual Basic toolbox during design mode.</span></span>

<span data-ttu-id="22ff6-113">A entrada de **controle** marca um objeto como um controle.</span><span class="sxs-lookup"><span data-stu-id="22ff6-113">The **Control** entry marks an object as a control.</span></span> <span data-ttu-id="22ff6-114">Essa entrada é frequentemente usada por contêineres para preencher caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="22ff6-114">This entry is often used by containers to fill in dialog boxes.</span></span> <span data-ttu-id="22ff6-115">O contêiner usa essa subchave para determinar se um objeto deve ser incluído em uma caixa de diálogo que exibe controles.</span><span class="sxs-lookup"><span data-stu-id="22ff6-115">The container uses this sub-key to determine whether to include an object in a dialog box that displays controls.</span></span>

<span data-ttu-id="22ff6-116">A subchave **insertável** também pode ser usada com controles, dependendo se o objeto pode agir somente como um objeto incorporado inserido sem recursos de controle especiais.</span><span class="sxs-lookup"><span data-stu-id="22ff6-116">The **Insertable** sub-key can also be used with controls, depending on whether the object can act only as an in-place embedded object with no special control features.</span></span> <span data-ttu-id="22ff6-117">Os objetos marcados com **insertáveis** aparecem na caixa de diálogo Inserir objeto de seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="22ff6-117">Objects marked with **Insertable** appear in the Insert Object dialog box of their container.</span></span> <span data-ttu-id="22ff6-118">A entrada **insertável** geralmente significa que o controle foi testado com contêineres que não são de controle.</span><span class="sxs-lookup"><span data-stu-id="22ff6-118">The **Insertable** entry generally means that the control has been tested with non-control containers.</span></span>

<span data-ttu-id="22ff6-119">As subchaves **insertáveis** e **Control** são opcionais.</span><span class="sxs-lookup"><span data-stu-id="22ff6-119">Both the **Insertable** and the **Control** sub-keys are optional.</span></span> <span data-ttu-id="22ff6-120">Um controle poderá omitir a subchave que pode ser **inserida** se não tiver sido projetada para trabalhar com contêineres mais antigos que não entendem controles.</span><span class="sxs-lookup"><span data-stu-id="22ff6-120">A control can omit the **Insertable** sub-key if it not designed to work with older containers that do not understand controls.</span></span> <span data-ttu-id="22ff6-121">Um controle pode omitir a chave de **controle** se ele for projetado apenas para funcionar com um contêiner específico e, portanto, não desejar ser inserido em outros contêineres.</span><span class="sxs-lookup"><span data-stu-id="22ff6-121">A control can omit the **Control** key if it is only designed to work with a specific container and thus does not wish to be inserted in other containers.</span></span>

<span data-ttu-id="22ff6-122">Os controles devem ter um verbo Properties, \_ Propriedades OLEIVERB, juntamente com quaisquer outros verbos aos quais eles dão suporte.</span><span class="sxs-lookup"><span data-stu-id="22ff6-122">Controls should have a Properties verb, OLEIVERB\_PROPERTIES, along with any other verbs they support.</span></span> <span data-ttu-id="22ff6-123">O verbo Properties, bem como o verbo padrão OLEIVERB \_ principal, instrui o controle a exibir sua folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="22ff6-123">The Properties verb, as well as the standard verb OLEIVERB\_PRIMARY, instructs the control to display its property sheet.</span></span> <span data-ttu-id="22ff6-124">O verbo de propriedades é exibido como o item de propriedades no menu do contêiner quando o controle está ativo.</span><span class="sxs-lookup"><span data-stu-id="22ff6-124">The Properties verb is displayed as the Properties item on the container's menu when the control is active.</span></span> <span data-ttu-id="22ff6-125">Dessa forma, o controle pode exibir sua própria página de propriedades, permitindo uma funcionalidade útil para o usuário final, mesmo que o contêiner não manipule controles.</span><span class="sxs-lookup"><span data-stu-id="22ff6-125">This way, the control can display its own property page allowing some useful functionality to the end user, even if the container does not handle controls.</span></span>

<span data-ttu-id="22ff6-126">Um controle define a chave **MiscStatus** para se descrever para possíveis contêineres.</span><span class="sxs-lookup"><span data-stu-id="22ff6-126">A control defines the **MiscStatus** key to describe itself to potential containers.</span></span> <span data-ttu-id="22ff6-127">Os bits assumem os valores de [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc)e os controles adicionam vários valores a essa enumeração.</span><span class="sxs-lookup"><span data-stu-id="22ff6-127">The bits take on the values from [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc), and controls add several values to this enumeration.</span></span> <span data-ttu-id="22ff6-128">Consulte os valores de enumeração **OLEMISC** para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="22ff6-128">See the **OLEMISC** enumeration values for more information.</span></span> <span data-ttu-id="22ff6-129">O cliente pode obter essas informações chamando [**IOleObject:: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) sem precisar instanciar o controle primeiro.</span><span class="sxs-lookup"><span data-stu-id="22ff6-129">The client can obtain this information by calling [**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) without having to instantiate the control first.</span></span>

<span data-ttu-id="22ff6-130">Por fim, a **versão** descreve a versão do controle que deve corresponder à versão da biblioteca de tipos associada a este controle.</span><span class="sxs-lookup"><span data-stu-id="22ff6-130">Finally, **Version** describes the version of the control which should match the version of the type library associated with this control.</span></span>

<span data-ttu-id="22ff6-131">Também nas informações de tipo de um controle, o controle atributo marca uma entrada coclasse como descrevendo um controle.</span><span class="sxs-lookup"><span data-stu-id="22ff6-131">Also in the type information for a control, the attribute control marks a coclass entry as describing a control.</span></span>

 

 
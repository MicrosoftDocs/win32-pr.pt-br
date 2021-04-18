---
title: Registro automático para controles
description: Registro automático para controles
ms.assetid: 0fff07e5-10bb-4052-8eb1-021efcb66d6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdf2d71dcee1727031dd6ad9d55d88baf86a6b3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105783685"
---
# <a name="self-registration-for-controls"></a><span data-ttu-id="90351-103">Registro automático para controles</span><span class="sxs-lookup"><span data-stu-id="90351-103">Self Registration for Controls</span></span>

<span data-ttu-id="90351-104">Os controles ActiveX devem dar suporte ao auto-registro implementando as funções [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) .</span><span class="sxs-lookup"><span data-stu-id="90351-104">ActiveX controls must support self-registration by implementing the [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) functions.</span></span> <span data-ttu-id="90351-105">Os controles ActiveX devem registrar todas as entradas de registro padrão para objetos incorporáveis e servidores de automação.</span><span class="sxs-lookup"><span data-stu-id="90351-105">ActiveX controls must register all of the standard registry entries for embeddable objects and automation servers.</span></span>

<span data-ttu-id="90351-106">Os controles ActiveX devem usar a API de categorias de componentes para se registrarem como um controle e registrar as categorias de componentes que exigem que um host dê suporte e quaisquer categorias implementadas pelo controle, consulte [categorias de componentes](component-categories.md).</span><span class="sxs-lookup"><span data-stu-id="90351-106">ActiveX controls must use the component categories API to register themselves as a control and register the component categories that they require a host to support and any categories that the control implements, see [Component Categories](component-categories.md).</span></span>

<span data-ttu-id="90351-107">Os controles ActiveX também devem registrar a chave do registro [ToolBoxBitmap32](toolboxbitmap32.md) , embora isso não seja obrigatório.</span><span class="sxs-lookup"><span data-stu-id="90351-107">ActiveX controls should also register the [ToolBoxBitmap32](toolboxbitmap32.md) registry key, although this is not mandatory.</span></span>

<span data-ttu-id="90351-108">A categoria de componente que pode ser inserido só deverá ser registrada se o controle for adequado para uso como um objeto de documento composto.</span><span class="sxs-lookup"><span data-stu-id="90351-108">The Insertable component category should be registered only if the control is suitable for use as a compound document object.</span></span> <span data-ttu-id="90351-109">É importante observar que um objeto de documento composto deve dar suporte a determinadas interfaces além do [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) mínimo necessário para um controle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="90351-109">It is important to note that a compound document object must support certain interfaces beyond the minimum [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) required for an ActiveX control.</span></span> <span data-ttu-id="90351-110">Embora um controle ActiveX possa ser qualificado como um objeto de documento composto, a documentação do controle deve indicar claramente o comportamento a ser esperado nessas circunstâncias.</span><span class="sxs-lookup"><span data-stu-id="90351-110">Although an ActiveX control may qualify as a compound document object, the control's documentation should clearly state what behavior to expect under these circumstances.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90351-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="90351-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90351-112">Controles</span><span class="sxs-lookup"><span data-stu-id="90351-112">Controls</span></span>](controls.md)
</dt> </dl>

 

 
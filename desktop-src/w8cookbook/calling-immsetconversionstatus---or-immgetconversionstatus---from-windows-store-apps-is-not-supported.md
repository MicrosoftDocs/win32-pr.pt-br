---
title: Não há suporte para a chamada de ImmSetConversionStatus () ou ImmGetConversionStatus () de aplicativos da Windows Store
description: Não há suporte para a chamada de ImmSetConversionStatus () ou ImmGetConversionStatus () de aplicativos da Windows Store
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b0846b56b1d6c2367c46e4adf82dac011c49fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641198"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a><span data-ttu-id="0dfdf-103">Não há suporte para a chamada de ImmSetConversionStatus () ou ImmGetConversionStatus () de aplicativos da Windows Store</span><span class="sxs-lookup"><span data-stu-id="0dfdf-103">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from Windows Store apps is not supported</span></span>

## <a name="platforms"></a><span data-ttu-id="0dfdf-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="0dfdf-104">Platforms</span></span>

<dl> <span data-ttu-id="0dfdf-105">Clientes-Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="0dfdf-105">Clients - windows 8.1</span></span>  
<span data-ttu-id="0dfdf-106">Servidores-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0dfdf-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="0dfdf-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0dfdf-107">Description</span></span>

<span data-ttu-id="0dfdf-108">Não há suporte para a chamada de ImmSetConversionStatus () ou ImmGetConversionStatus () de um aplicativo da Windows Store e isso pode causar resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-108">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from a Windows Store app is not supported and may cause unexpected results.</span></span>

## <a name="manifestations"></a><span data-ttu-id="0dfdf-109">Manifestações</span><span class="sxs-lookup"><span data-stu-id="0dfdf-109">Manifestations</span></span>

<span data-ttu-id="0dfdf-110">Na inicialização do aplicativo, o modo IME é definido com os seguintes padrões:</span><span class="sxs-lookup"><span data-stu-id="0dfdf-110">At application start up, the IME mode is set to the following defaults:</span></span>



|          | <span data-ttu-id="0dfdf-111">Painel de entrada de software</span><span class="sxs-lookup"><span data-stu-id="0dfdf-111">Software input panel</span></span> | <span data-ttu-id="0dfdf-112">Teclado de hardware</span><span class="sxs-lookup"><span data-stu-id="0dfdf-112">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="0dfdf-113">KOR, JPN</span><span class="sxs-lookup"><span data-stu-id="0dfdf-113">KOR, JPN</span></span> | <span data-ttu-id="0dfdf-114">Ativado</span><span class="sxs-lookup"><span data-stu-id="0dfdf-114">On</span></span>                   | <span data-ttu-id="0dfdf-115">Desativado</span><span class="sxs-lookup"><span data-stu-id="0dfdf-115">Off</span></span>               |
| <span data-ttu-id="0dfdf-116">CHS, CHT</span><span class="sxs-lookup"><span data-stu-id="0dfdf-116">CHS, CHT</span></span> | <span data-ttu-id="0dfdf-117">Ativado</span><span class="sxs-lookup"><span data-stu-id="0dfdf-117">On</span></span>                   | <span data-ttu-id="0dfdf-118">Ativado</span><span class="sxs-lookup"><span data-stu-id="0dfdf-118">On</span></span>                |



 

## <a name="solution"></a><span data-ttu-id="0dfdf-119">Solução</span><span class="sxs-lookup"><span data-stu-id="0dfdf-119">Solution</span></span>

<span data-ttu-id="0dfdf-120">Os desenvolvedores podem controlar o modo IME padrão especificando um valor de escopo de entrada para o campo.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-120">Developers can control the default IME mode by specifying an input scope value for the field.</span></span>

<span data-ttu-id="0dfdf-121">O modo IME para um escopo de entrada especificado é determinado por cada IME.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-121">The IME mode for a specified input scope is determined by each IME.</span></span> <span data-ttu-id="0dfdf-122">Os desenvolvedores não podem especificar o modo IME.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-122">Developers cannot specify the IME mode.</span></span>

## <a name="resources"></a><span data-ttu-id="0dfdf-123">Recursos</span><span class="sxs-lookup"><span data-stu-id="0dfdf-123">Resources</span></span>

-   [<span data-ttu-id="0dfdf-124">Enumeração InputScope</span><span class="sxs-lookup"><span data-stu-id="0dfdf-124">InputScope Enumeration</span></span>](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [<span data-ttu-id="0dfdf-125">ImmSetConversionStatus</span><span class="sxs-lookup"><span data-stu-id="0dfdf-125">ImmSetConversionStatus</span></span>](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   <span data-ttu-id="0dfdf-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="0dfdf-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span></span>

 

 
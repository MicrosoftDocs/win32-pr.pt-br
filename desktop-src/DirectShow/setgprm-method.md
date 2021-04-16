---
description: O método SetGPRM define o registro de parâmetro geral especificado como o valor especificado.
ms.assetid: ded28f2a-5e40-4f76-9ed4-de10296529e1
title: Método SetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e7492c599cde4c074c1a806f897edf3a8fe0a4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105757868"
---
# <a name="setgprm-method"></a><span data-ttu-id="350b0-103">Método SetGPRM</span><span class="sxs-lookup"><span data-stu-id="350b0-103">SetGPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="350b0-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="350b0-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="350b0-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="350b0-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="350b0-106">O `SetGPRM` método define o registro de parâmetro geral especificado para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="350b0-106">The `SetGPRM` method sets the specified general parameter register to the specified value.</span></span>

``` syntax
MSWebDVD.SetGPRM(iIndex, nValue)
```

## <a name="parameters"></a><span data-ttu-id="350b0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="350b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="350b0-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="350b0-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="350b0-109">Especifica o registro de parâmetro geral a ser definido como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="350b0-109">Specifies the general parameter register to set as an Integer.</span></span> <span data-ttu-id="350b0-110">O valor inteiro deve variar de 0 a 15.</span><span class="sxs-lookup"><span data-stu-id="350b0-110">The Integer value must range from 0 through 15.</span></span>

</dd> <dt>

<span data-ttu-id="350b0-111"><span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*nvalor*</span><span class="sxs-lookup"><span data-stu-id="350b0-111"><span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*nValue*</span></span>
</dt> <dd>

<span data-ttu-id="350b0-112">Especifica o novo valor para o registro como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="350b0-112">Specifies the new value for the register as an Integer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="350b0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="350b0-113">Remarks</span></span>

<span data-ttu-id="350b0-114">Registros de parâmetro gerais, ou GPRMs, são registros de 16 bits que cada disco pode usar de maneiras exclusivas para o armazenamento temporário de dados.</span><span class="sxs-lookup"><span data-stu-id="350b0-114">General parameter registers, or GPRMs, are 16-bit registers that each disc can use in unique ways for temporary data storage.</span></span> <span data-ttu-id="350b0-115">Um aplicativo de Player não precisa acessar esses registros para qualquer reprodução padrão ou controle de navegação usando o objeto **MSWebDVD** .</span><span class="sxs-lookup"><span data-stu-id="350b0-115">A player application does not need to access these registers for any standard playback or navigation control using the **MSWebDVD** object.</span></span> <span data-ttu-id="350b0-116">Esse método é fornecido para aplicativos de Player que implementam a funcionalidade avançada.</span><span class="sxs-lookup"><span data-stu-id="350b0-116">This method is provided for player applications implementing advanced functionality.</span></span> <span data-ttu-id="350b0-117">Não tente modificar o GPRMs diretamente, a menos que você tenha um conhecimento completo sobre a especificação de DVD e as maneiras em que os GPRMs são usados no disco específico a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="350b0-117">Do not attempt to modify the GPRMs directly unless you have a thorough knowledge of the DVD specification and the ways in which the GPRMs are used on the particular disc to be played.</span></span> <span data-ttu-id="350b0-118">A alteração desses valores pode resultar em um comportamento imprevisível.</span><span class="sxs-lookup"><span data-stu-id="350b0-118">Changing these values can result in unpredictable behavior.</span></span>

 

 




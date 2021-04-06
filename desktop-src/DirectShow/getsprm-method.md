---
description: O método GetSPRM recupera o registro de parâmetro do sistema especificado.
ms.assetid: c6177f43-2809-4ef2-bc94-ac9a28f94621
title: Método GetSPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8b6898902eda55e0e877878343a25d82d03660
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919703"
---
# <a name="getsprm-method"></a><span data-ttu-id="92a1d-103">Método GetSPRM</span><span class="sxs-lookup"><span data-stu-id="92a1d-103">GetSPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="92a1d-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="92a1d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="92a1d-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="92a1d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="92a1d-106">O `GetSPRM` método recupera o registro de parâmetro do sistema especificado.</span><span class="sxs-lookup"><span data-stu-id="92a1d-106">The `GetSPRM` method retrieves the specified system parameter register.</span></span>

``` syntax
[ iSPRM = ] MSWebDVD.GetSPRM(iIndex)
```

## <a name="parameters"></a><span data-ttu-id="92a1d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92a1d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92a1d-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="92a1d-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="92a1d-109">Especifica o registro cujo valor você deseja recuperar como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="92a1d-109">Specifies the register whose value you want to retrieve as an Integer.</span></span> <span data-ttu-id="92a1d-110">O número inteiro deve variar de 0 a 23.</span><span class="sxs-lookup"><span data-stu-id="92a1d-110">The Integer must range from 0 through 23.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92a1d-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="92a1d-111">Return Value</span></span>

<span data-ttu-id="92a1d-112">Retorna um valor inteiro que representa o conteúdo do registro especificado.</span><span class="sxs-lookup"><span data-stu-id="92a1d-112">Returns an integer value representing the contents of the specified register.</span></span>

## <a name="remarks"></a><span data-ttu-id="92a1d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="92a1d-113">Remarks</span></span>

<span data-ttu-id="92a1d-114">O disco controla os registros de parâmetro do sistema (SPRMs).</span><span class="sxs-lookup"><span data-stu-id="92a1d-114">The disc controls system parameter registers (SPRMs).</span></span> <span data-ttu-id="92a1d-115">Um aplicativo de Player não precisa acessar esses registros para qualquer funcionalidade de navegação padrão.</span><span class="sxs-lookup"><span data-stu-id="92a1d-115">A player application doesn't need to access these registers for any standard navigation functionality.</span></span> <span data-ttu-id="92a1d-116">SPRMs representa o status do Player.</span><span class="sxs-lookup"><span data-stu-id="92a1d-116">SPRMs represent the status of the player.</span></span> <span data-ttu-id="92a1d-117">Cada um tem um significado, definido por preferências do usuário, comandos de disco e outras ocorrências das quais um aplicativo não tem controle direto.</span><span class="sxs-lookup"><span data-stu-id="92a1d-117">Each one has a meaning, set by user preferences, disc commands, and other occurrences that an application has no direct control over.</span></span> <span data-ttu-id="92a1d-118">Um aplicativo pode ler esses registros, mas não pode gravar neles.</span><span class="sxs-lookup"><span data-stu-id="92a1d-118">An application can read these registers but cannot write to them.</span></span> <span data-ttu-id="92a1d-119">Para usar esses registros com eficiência, você provavelmente precisará de um conhecimento mais detalhado dos comandos de navegação do DVD do que é fornecido nesta documentação.</span><span class="sxs-lookup"><span data-stu-id="92a1d-119">To use these registers effectively, you will probably need a more detailed knowledge of the DVD navigation commands than is provided in this documentation.</span></span> <span data-ttu-id="92a1d-120">A tabela a seguir mostra o conteúdo de cada registro.</span><span class="sxs-lookup"><span data-stu-id="92a1d-120">The following table shows the contents of each register.</span></span> <span data-ttu-id="92a1d-121">Para obter informações mais detalhadas sobre o conteúdo do registro, consulte [ **IDvdInfo2:: GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)</span><span class="sxs-lookup"><span data-stu-id="92a1d-121">For more detailed information on the register contents, see [**IDvdInfo2::GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)</span></span>



| <span data-ttu-id="92a1d-122">Registre-se</span><span class="sxs-lookup"><span data-stu-id="92a1d-122">Register</span></span> | <span data-ttu-id="92a1d-123">Sumário</span><span class="sxs-lookup"><span data-stu-id="92a1d-123">Contents</span></span>                        |
|----------|---------------------------------|
| <span data-ttu-id="92a1d-124">0</span><span class="sxs-lookup"><span data-stu-id="92a1d-124">0</span></span>        | <span data-ttu-id="92a1d-125">Código de idioma do menu</span><span class="sxs-lookup"><span data-stu-id="92a1d-125">Menu language code</span></span>              |
| <span data-ttu-id="92a1d-126">1</span><span class="sxs-lookup"><span data-stu-id="92a1d-126">1</span></span>        | <span data-ttu-id="92a1d-127">Número do fluxo de áudio</span><span class="sxs-lookup"><span data-stu-id="92a1d-127">Audio stream number</span></span>             |
| <span data-ttu-id="92a1d-128">2</span><span class="sxs-lookup"><span data-stu-id="92a1d-128">2</span></span>        | <span data-ttu-id="92a1d-129">Número de fluxo da subimagem</span><span class="sxs-lookup"><span data-stu-id="92a1d-129">Subpicture stream number</span></span>        |
| <span data-ttu-id="92a1d-130">3</span><span class="sxs-lookup"><span data-stu-id="92a1d-130">3</span></span>        | <span data-ttu-id="92a1d-131">Número do ângulo atual</span><span class="sxs-lookup"><span data-stu-id="92a1d-131">Current angle number</span></span>            |
| <span data-ttu-id="92a1d-132">4</span><span class="sxs-lookup"><span data-stu-id="92a1d-132">4</span></span>        | <span data-ttu-id="92a1d-133">Número do título atual</span><span class="sxs-lookup"><span data-stu-id="92a1d-133">Current title number</span></span>            |
| <span data-ttu-id="92a1d-134">5</span><span class="sxs-lookup"><span data-stu-id="92a1d-134">5</span></span>        | <span data-ttu-id="92a1d-135">Número do título</span><span class="sxs-lookup"><span data-stu-id="92a1d-135">Title number</span></span>                    |
| <span data-ttu-id="92a1d-136">6</span><span class="sxs-lookup"><span data-stu-id="92a1d-136">6</span></span>        | <span data-ttu-id="92a1d-137">Número de PGC</span><span class="sxs-lookup"><span data-stu-id="92a1d-137">PGC number</span></span>                      |
| <span data-ttu-id="92a1d-138">7</span><span class="sxs-lookup"><span data-stu-id="92a1d-138">7</span></span>        | <span data-ttu-id="92a1d-139">Número do capítulo atual (PTT)</span><span class="sxs-lookup"><span data-stu-id="92a1d-139">Current chapter number (PTT)</span></span>    |
| <span data-ttu-id="92a1d-140">8</span><span class="sxs-lookup"><span data-stu-id="92a1d-140">8</span></span>        | <span data-ttu-id="92a1d-141">Número do botão realçado</span><span class="sxs-lookup"><span data-stu-id="92a1d-141">Highlighted button number</span></span>       |
| <span data-ttu-id="92a1d-142">9</span><span class="sxs-lookup"><span data-stu-id="92a1d-142">9</span></span>        | <span data-ttu-id="92a1d-143">Temporizador de navegação</span><span class="sxs-lookup"><span data-stu-id="92a1d-143">Navigation timer</span></span>                |
| <span data-ttu-id="92a1d-144">10</span><span class="sxs-lookup"><span data-stu-id="92a1d-144">10</span></span>       | <span data-ttu-id="92a1d-145">Salto de PGC para navegação.</span><span class="sxs-lookup"><span data-stu-id="92a1d-145">PGC jump for nav.</span></span> <span data-ttu-id="92a1d-146">temporizador</span><span class="sxs-lookup"><span data-stu-id="92a1d-146">timer</span></span>         |
| <span data-ttu-id="92a1d-147">11</span><span class="sxs-lookup"><span data-stu-id="92a1d-147">11</span></span>       | <span data-ttu-id="92a1d-148">Modo de apresentação de áudio do karaokê</span><span class="sxs-lookup"><span data-stu-id="92a1d-148">Karaoke audio presentation mode</span></span> |
| <span data-ttu-id="92a1d-149">12</span><span class="sxs-lookup"><span data-stu-id="92a1d-149">12</span></span>       | <span data-ttu-id="92a1d-150">Código de país/região do PML</span><span class="sxs-lookup"><span data-stu-id="92a1d-150">PML country/region code</span></span>         |
| <span data-ttu-id="92a1d-151">13</span><span class="sxs-lookup"><span data-stu-id="92a1d-151">13</span></span>       | <span data-ttu-id="92a1d-152">PML</span><span class="sxs-lookup"><span data-stu-id="92a1d-152">PML</span></span>                             |
| <span data-ttu-id="92a1d-153">14</span><span class="sxs-lookup"><span data-stu-id="92a1d-153">14</span></span>       | <span data-ttu-id="92a1d-154">Configuração de vídeo</span><span class="sxs-lookup"><span data-stu-id="92a1d-154">Video setting</span></span>                   |
| <span data-ttu-id="92a1d-155">15</span><span class="sxs-lookup"><span data-stu-id="92a1d-155">15</span></span>       | <span data-ttu-id="92a1d-156">Funcionalidade de áudio</span><span class="sxs-lookup"><span data-stu-id="92a1d-156">Audio capability</span></span>                |
| <span data-ttu-id="92a1d-157">16</span><span class="sxs-lookup"><span data-stu-id="92a1d-157">16</span></span>       | <span data-ttu-id="92a1d-158">Idioma do áudio</span><span class="sxs-lookup"><span data-stu-id="92a1d-158">Audio language</span></span>                  |
| <span data-ttu-id="92a1d-159">17</span><span class="sxs-lookup"><span data-stu-id="92a1d-159">17</span></span>       | <span data-ttu-id="92a1d-160">Extensão de idioma de áudio</span><span class="sxs-lookup"><span data-stu-id="92a1d-160">Audio language extension</span></span>        |
| <span data-ttu-id="92a1d-161">18</span><span class="sxs-lookup"><span data-stu-id="92a1d-161">18</span></span>       | <span data-ttu-id="92a1d-162">Idioma da subimagem</span><span class="sxs-lookup"><span data-stu-id="92a1d-162">Subpicture language</span></span>             |
| <span data-ttu-id="92a1d-163">19</span><span class="sxs-lookup"><span data-stu-id="92a1d-163">19</span></span>       | <span data-ttu-id="92a1d-164">Extensão da linguagem de subimagem</span><span class="sxs-lookup"><span data-stu-id="92a1d-164">Subpicture language extension</span></span>   |
| <span data-ttu-id="92a1d-165">20</span><span class="sxs-lookup"><span data-stu-id="92a1d-165">20</span></span>       | <span data-ttu-id="92a1d-166">Código de região do Player</span><span class="sxs-lookup"><span data-stu-id="92a1d-166">Player region code</span></span>              |
| <span data-ttu-id="92a1d-167">21</span><span class="sxs-lookup"><span data-stu-id="92a1d-167">21</span></span>       | <span data-ttu-id="92a1d-168">Reservado</span><span class="sxs-lookup"><span data-stu-id="92a1d-168">Reserved</span></span>                        |
| <span data-ttu-id="92a1d-169">22</span><span class="sxs-lookup"><span data-stu-id="92a1d-169">22</span></span>       | <span data-ttu-id="92a1d-170">Reservado</span><span class="sxs-lookup"><span data-stu-id="92a1d-170">Reserved</span></span>                        |
| <span data-ttu-id="92a1d-171">23</span><span class="sxs-lookup"><span data-stu-id="92a1d-171">23</span></span>       | <span data-ttu-id="92a1d-172">Reservado</span><span class="sxs-lookup"><span data-stu-id="92a1d-172">Reserved</span></span>                        |



 

## <a name="see-also"></a><span data-ttu-id="92a1d-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="92a1d-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92a1d-174">**GetGPRM**</span><span class="sxs-lookup"><span data-stu-id="92a1d-174">**GetGPRM**</span></span>](getgprm-method.md)
</dt> <dt>

[<span data-ttu-id="92a1d-175">**SetGPRM**</span><span class="sxs-lookup"><span data-stu-id="92a1d-175">**SetGPRM**</span></span>](setgprm-method.md)
</dt> </dl>

 

 




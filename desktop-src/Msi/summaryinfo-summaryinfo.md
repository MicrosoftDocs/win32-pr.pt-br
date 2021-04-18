---
description: A Propriedade Property do objeto SummaryInfo define ou Obtém o valor para a propriedade especificada no fluxo de informações de resumo.
ms.assetid: 8e8f0987-c92b-43f3-a61a-35099188c629
title: Propriedade SummaryInfo. Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e51773a930b8868e31a7e88848300a62b717912
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754341"
---
# <a name="summaryinfoproperty-property"></a><span data-ttu-id="5d314-103">Propriedade SummaryInfo. Property</span><span class="sxs-lookup"><span data-stu-id="5d314-103">SummaryInfo.Property property</span></span>

<span data-ttu-id="5d314-104">A propriedade **Property** do objeto [**SummaryInfo**](summaryinfo-object.md) define ou Obtém o valor para a propriedade especificada no fluxo de informações de resumo.</span><span class="sxs-lookup"><span data-stu-id="5d314-104">The **Property** property of the [**SummaryInfo**](summaryinfo-object.md) object sets or gets the value for the specified property in the summary information stream.</span></span> <span data-ttu-id="5d314-105">As propriedades são lidas quando o objeto [**SummaryInfo**](summaryinfo-object.md) é criado, mas eles não são gravados até que o método [**Persist**](summaryinfo-persist.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="5d314-105">The properties are read when the [**SummaryInfo**](summaryinfo-object.md) object is created, but they are not written until the [**Persist**](summaryinfo-persist.md) method is called.</span></span> <span data-ttu-id="5d314-106">Definir uma propriedade como Empty causa sua remoção; da mesma forma, a solicitação de uma propriedade inexistente retorna um valor vazio.</span><span class="sxs-lookup"><span data-stu-id="5d314-106">Setting a property to Empty causes its removal; likewise, requesting a nonexistent property returns an Empty value.</span></span> <span data-ttu-id="5d314-107">Caso contrário, os valores podem ser transferidos como cadeias de caracteres, inteiros ou tipos de data (data e hora).</span><span class="sxs-lookup"><span data-stu-id="5d314-107">Otherwise values may be transferred as strings, integers, or date (date time) types.</span></span>

<span data-ttu-id="5d314-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="5d314-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d314-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d314-109">Syntax</span></span>


```JScript
propVal = SummaryInfo.Property
```



## <a name="property-value"></a><span data-ttu-id="5d314-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5d314-110">Property value</span></span>

<span data-ttu-id="5d314-111">A ID de propriedade necessária de uma das propriedades de resumo.</span><span class="sxs-lookup"><span data-stu-id="5d314-111">Required property ID of one of the summary properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d314-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d314-112">Remarks</span></span>

<span data-ttu-id="5d314-113">**IDs de propriedade de resumo padrão**</span><span class="sxs-lookup"><span data-stu-id="5d314-113">**Standard Summary Property IDs**</span></span>

<span data-ttu-id="5d314-114">(não é uma enumeração)</span><span class="sxs-lookup"><span data-stu-id="5d314-114">(not an enumeration)</span></span>



| <span data-ttu-id="5d314-115">Nome do parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d314-115">Parameter name</span></span>     | <span data-ttu-id="5d314-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5d314-116">Value</span></span> | <span data-ttu-id="5d314-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d314-117">Description</span></span>                                       |
|--------------------|-------|---------------------------------------------------|
| <span data-ttu-id="5d314-118">\_dicionário PID</span><span class="sxs-lookup"><span data-stu-id="5d314-118">PID\_DICTIONARY</span></span>    | <span data-ttu-id="5d314-119">0</span><span class="sxs-lookup"><span data-stu-id="5d314-119">0</span></span>     | <span data-ttu-id="5d314-120">Formato especial, não suporte pelo objeto SummaryInfo</span><span class="sxs-lookup"><span data-stu-id="5d314-120">Special format, not support by SummaryInfo object</span></span> |
| <span data-ttu-id="5d314-121">\_página de código PID</span><span class="sxs-lookup"><span data-stu-id="5d314-121">PID\_CODEPAGE</span></span>      | <span data-ttu-id="5d314-122">1</span><span class="sxs-lookup"><span data-stu-id="5d314-122">1</span></span>     | <span data-ttu-id="5d314-123">\_I2 VT</span><span class="sxs-lookup"><span data-stu-id="5d314-123">VT\_I2</span></span>                                            |
| <span data-ttu-id="5d314-124">título da PID \_</span><span class="sxs-lookup"><span data-stu-id="5d314-124">PID\_TITLE</span></span>         | <span data-ttu-id="5d314-125">2</span><span class="sxs-lookup"><span data-stu-id="5d314-125">2</span></span>     | <span data-ttu-id="5d314-126">a VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="5d314-126">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="5d314-127">\_entidade PID</span><span class="sxs-lookup"><span data-stu-id="5d314-127">PID\_SUBJECT</span></span>       | <span data-ttu-id="5d314-128">3</span><span class="sxs-lookup"><span data-stu-id="5d314-128">3</span></span>     | <span data-ttu-id="5d314-129">a VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="5d314-129">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="5d314-130">autor da PID \_</span><span class="sxs-lookup"><span data-stu-id="5d314-130">PID\_AUTHOR</span></span>        | <span data-ttu-id="5d314-131">4</span><span class="sxs-lookup"><span data-stu-id="5d314-131">4</span></span>     | <span data-ttu-id="5d314-132">a VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="5d314-132">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="5d314-133">\_palavras-chave PID</span><span class="sxs-lookup"><span data-stu-id="5d314-133">PID\_KEYWORDS</span></span>      | <span data-ttu-id="5d314-134">5</span><span class="sxs-lookup"><span data-stu-id="5d314-134">5</span></span>     | <span data-ttu-id="5d314-135">a VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="5d314-135">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="5d314-136">Comentários de PID \_</span><span class="sxs-lookup"><span data-stu-id="5d314-136">PID\_COMMENTS</span></span>      | <span data-ttu-id="5d314-137">6</span><span class="sxs-lookup"><span data-stu-id="5d314-137">6</span></span>     | <span data-ttu-id="5d314-138">a VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="5d314-138">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="5d314-139">\_modelo PID</span><span class="sxs-lookup"><span data-stu-id="5d314-139">PID\_TEMPLATE</span></span>      | <span data-ttu-id="5d314-140">7</span><span class="sxs-lookup"><span data-stu-id="5d314-140">7</span></span>     | <span data-ttu-id="5d314-141">a VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="5d314-141">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="5d314-142">DTI \_ LASTAUTHOR</span><span class="sxs-lookup"><span data-stu-id="5d314-142">PID\_LASTAUTHOR</span></span>    | <span data-ttu-id="5d314-143">8</span><span class="sxs-lookup"><span data-stu-id="5d314-143">8</span></span>     | <span data-ttu-id="5d314-144">a VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="5d314-144">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="5d314-145">DTI \_ REVNUMBER</span><span class="sxs-lookup"><span data-stu-id="5d314-145">PID\_REVNUMBER</span></span>     | <span data-ttu-id="5d314-146">9</span><span class="sxs-lookup"><span data-stu-id="5d314-146">9</span></span>     | <span data-ttu-id="5d314-147">a VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="5d314-147">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="5d314-148">PID \_ EditTime</span><span class="sxs-lookup"><span data-stu-id="5d314-148">PID\_EDITTIME</span></span>      | <span data-ttu-id="5d314-149">10</span><span class="sxs-lookup"><span data-stu-id="5d314-149">10</span></span>    | <span data-ttu-id="5d314-150">FILETIME do VT \_</span><span class="sxs-lookup"><span data-stu-id="5d314-150">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="5d314-151">DTI \_ LASTPRINTED</span><span class="sxs-lookup"><span data-stu-id="5d314-151">PID\_LASTPRINTED</span></span>   | <span data-ttu-id="5d314-152">11</span><span class="sxs-lookup"><span data-stu-id="5d314-152">11</span></span>    | <span data-ttu-id="5d314-153">FILETIME do VT \_</span><span class="sxs-lookup"><span data-stu-id="5d314-153">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="5d314-154">PID \_ criar \_ DTM</span><span class="sxs-lookup"><span data-stu-id="5d314-154">PID\_CREATE\_DTM</span></span>   | <span data-ttu-id="5d314-155">12</span><span class="sxs-lookup"><span data-stu-id="5d314-155">12</span></span>    | <span data-ttu-id="5d314-156">FILETIME do VT \_</span><span class="sxs-lookup"><span data-stu-id="5d314-156">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="5d314-157">DTI \_ LASTSAVE \_ DTM</span><span class="sxs-lookup"><span data-stu-id="5d314-157">PID\_LASTSAVE\_DTM</span></span> | <span data-ttu-id="5d314-158">13</span><span class="sxs-lookup"><span data-stu-id="5d314-158">13</span></span>    | <span data-ttu-id="5d314-159">FILETIME do VT \_</span><span class="sxs-lookup"><span data-stu-id="5d314-159">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="5d314-160">DTI \_ PageCount</span><span class="sxs-lookup"><span data-stu-id="5d314-160">PID\_PAGECOUNT</span></span>     | <span data-ttu-id="5d314-161">14</span><span class="sxs-lookup"><span data-stu-id="5d314-161">14</span></span>    | <span data-ttu-id="5d314-162">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="5d314-162">VT\_I4</span></span>                                            |
| <span data-ttu-id="5d314-163">DTI \_ WORDCOUNT</span><span class="sxs-lookup"><span data-stu-id="5d314-163">PID\_WORDCOUNT</span></span>     | <span data-ttu-id="5d314-164">15</span><span class="sxs-lookup"><span data-stu-id="5d314-164">15</span></span>    | <span data-ttu-id="5d314-165">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="5d314-165">VT\_I4</span></span>                                            |
| <span data-ttu-id="5d314-166">DTI \_ charCount</span><span class="sxs-lookup"><span data-stu-id="5d314-166">PID\_CHARCOUNT</span></span>     | <span data-ttu-id="5d314-167">16</span><span class="sxs-lookup"><span data-stu-id="5d314-167">16</span></span>    | <span data-ttu-id="5d314-168">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="5d314-168">VT\_I4</span></span>                                            |
| <span data-ttu-id="5d314-169">miniatura de PID \_</span><span class="sxs-lookup"><span data-stu-id="5d314-169">PID\_THUMBNAIL</span></span>     | <span data-ttu-id="5d314-170">17</span><span class="sxs-lookup"><span data-stu-id="5d314-170">17</span></span>    | <span data-ttu-id="5d314-171">VT \_ CF (sem suporte)</span><span class="sxs-lookup"><span data-stu-id="5d314-171">VT\_CF (not supported)</span></span>                            |
| <span data-ttu-id="5d314-172">\_APPNAME PID</span><span class="sxs-lookup"><span data-stu-id="5d314-172">PID\_APPNAME</span></span>       | <span data-ttu-id="5d314-173">18</span><span class="sxs-lookup"><span data-stu-id="5d314-173">18</span></span>    | <span data-ttu-id="5d314-174">a VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="5d314-174">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="5d314-175">segurança de PID \_</span><span class="sxs-lookup"><span data-stu-id="5d314-175">PID\_SECURITY</span></span>      | <span data-ttu-id="5d314-176">19</span><span class="sxs-lookup"><span data-stu-id="5d314-176">19</span></span>    | <span data-ttu-id="5d314-177">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="5d314-177">VT\_I4</span></span>                                            |



 

<span data-ttu-id="5d314-178">**Tipos de dados de propriedade**</span><span class="sxs-lookup"><span data-stu-id="5d314-178">**Property Data Types**</span></span>

<span data-ttu-id="5d314-179">(não é uma enumeração)</span><span class="sxs-lookup"><span data-stu-id="5d314-179">(not an enumeration)</span></span>



| <span data-ttu-id="5d314-180">Nome do parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d314-180">Parameter name</span></span> | <span data-ttu-id="5d314-181">Valor</span><span class="sxs-lookup"><span data-stu-id="5d314-181">Value</span></span> | <span data-ttu-id="5d314-182">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d314-182">Description</span></span>                                                                              |
|----------------|-------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d314-183">\_I2 VT</span><span class="sxs-lookup"><span data-stu-id="5d314-183">VT\_I2</span></span>         | <span data-ttu-id="5d314-184">2</span><span class="sxs-lookup"><span data-stu-id="5d314-184">2</span></span>     | <span data-ttu-id="5d314-185">inteiro de 16 bits</span><span class="sxs-lookup"><span data-stu-id="5d314-185">16-bit integer</span></span>                                                                           |
| <span data-ttu-id="5d314-186">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="5d314-186">VT\_I4</span></span>         | <span data-ttu-id="5d314-187">3</span><span class="sxs-lookup"><span data-stu-id="5d314-187">3</span></span>     | <span data-ttu-id="5d314-188">Inteiro de 32 bits</span><span class="sxs-lookup"><span data-stu-id="5d314-188">32-bit integer</span></span>                                                                           |
| <span data-ttu-id="5d314-189">a VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="5d314-189">VT\_LPSTR</span></span>      | <span data-ttu-id="5d314-190">30</span><span class="sxs-lookup"><span data-stu-id="5d314-190">30</span></span>    | <span data-ttu-id="5d314-191">String</span><span class="sxs-lookup"><span data-stu-id="5d314-191">String</span></span>                                                                                   |
| <span data-ttu-id="5d314-192">FILETIME do VT \_</span><span class="sxs-lookup"><span data-stu-id="5d314-192">VT\_FILETIME</span></span>   | <span data-ttu-id="5d314-193">64</span><span class="sxs-lookup"><span data-stu-id="5d314-193">64</span></span>    | <span data-ttu-id="5d314-194">Data e hora (FILETIME, convertido em hora da variante)</span><span class="sxs-lookup"><span data-stu-id="5d314-194">Date time (FILETIME, converted to Variant time)</span></span>                                          |
| <span data-ttu-id="5d314-195">VT \_ CF</span><span class="sxs-lookup"><span data-stu-id="5d314-195">VT\_CF</span></span>         | <span data-ttu-id="5d314-196">71</span><span class="sxs-lookup"><span data-stu-id="5d314-196">71</span></span>    | <span data-ttu-id="5d314-197">Formato da área de transferência + dados, não manipulados pelo objeto [**SummaryInfo**](summaryinfo-object.md)</span><span class="sxs-lookup"><span data-stu-id="5d314-197">Clipboard format + data, not handled by [**SummaryInfo**](summaryinfo-object.md) object</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="5d314-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d314-198">Requirements</span></span>



| <span data-ttu-id="5d314-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d314-199">Requirement</span></span> | <span data-ttu-id="5d314-200">Valor</span><span class="sxs-lookup"><span data-stu-id="5d314-200">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d314-201">Versão</span><span class="sxs-lookup"><span data-stu-id="5d314-201">Version</span></span><br/> | <span data-ttu-id="5d314-202">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5d314-202">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5d314-203">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5d314-203">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5d314-204">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="5d314-204">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5d314-205">DLL</span><span class="sxs-lookup"><span data-stu-id="5d314-205">DLL</span></span><br/>     | <dl> <span data-ttu-id="5d314-206"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d314-206"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5d314-207">IID</span><span class="sxs-lookup"><span data-stu-id="5d314-207">IID</span></span><br/>     | <span data-ttu-id="5d314-208">IID \_ ISummaryInfo é definido como 000C109B-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5d314-208">IID\_ISummaryInfo is defined as 000C109B-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="5d314-209">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d314-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d314-210">**MsiSummaryInfoSetProperty**</span><span class="sxs-lookup"><span data-stu-id="5d314-210">**MsiSummaryInfoSetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)
</dt> <dt>

[<span data-ttu-id="5d314-211">**MsiSummaryInfoGetProperty**</span><span class="sxs-lookup"><span data-stu-id="5d314-211">**MsiSummaryInfoGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)
</dt> </dl>

 

 





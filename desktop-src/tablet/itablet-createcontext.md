---
description: Cria um objeto de contexto que descreve o dispositivo tablet especificado.
ms.assetid: 76f48485-a958-4457-9b87-73de73fa671e
title: 'Método ITablet:: CreateContext'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.CreateContext
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 9f1214f7f9e429b5f9b5b9614c2ccfc7fd1800b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837022"
---
# <a name="itabletcreatecontext-method"></a><span data-ttu-id="86254-103">Método ITablet:: CreateContext</span><span class="sxs-lookup"><span data-stu-id="86254-103">ITablet::CreateContext method</span></span>

<span data-ttu-id="86254-104">Cria um objeto de contexto que descreve o dispositivo tablet especificado.</span><span class="sxs-lookup"><span data-stu-id="86254-104">Creates a context object that describes the specified tablet device.</span></span>

## <a name="syntax"></a><span data-ttu-id="86254-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86254-105">Syntax</span></span>


```C++
HRESULT CreateContext(
  [in]      HWND                    hWnd,
  [in]      RECT                    *prcInput,
  [in]      DWORD                   dwOptions,
  [in]      TABLET_CONTEXT_SETTINGS *pTCS,
  [in]      CONTEXT_ENABLE_TYPE     cet,
  [out]     ITabletContext          **ppCtx,
  [in, out] TABLET_CONTEXT_ID       *pTcid,
  [in, out] PACKET_DESCRIPTION      **ppPD,
  [in]      ITabletEventSink        *pSink
);
```



## <a name="parameters"></a><span data-ttu-id="86254-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86254-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86254-107">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86254-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86254-108">A janela à qual o contexto do Tablet será anexado.</span><span class="sxs-lookup"><span data-stu-id="86254-108">The window to which the tablet context will be attached.</span></span>

</dd> <dt>

<span data-ttu-id="86254-109">*prcInput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86254-109">*prcInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86254-110">\[em, exclusivo\]</span><span class="sxs-lookup"><span data-stu-id="86254-110">\[in, unique\]</span></span>

<span data-ttu-id="86254-111">O retângulo de entrada à tinta.</span><span class="sxs-lookup"><span data-stu-id="86254-111">The ink input rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="86254-112">*dwOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86254-112">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86254-113">Sinalizadores que definem opções de contexto do Tablet.</span><span class="sxs-lookup"><span data-stu-id="86254-113">Flags that set tablet context options.</span></span>

</dd> <dt>

<span data-ttu-id="86254-114">*pTCS* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86254-114">*pTCS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86254-115">\[em, exclusivo\]</span><span class="sxs-lookup"><span data-stu-id="86254-115">\[in, unique\]</span></span>

<span data-ttu-id="86254-116">Informações detalhadas sobre o contexto do Tablet a ser criado.</span><span class="sxs-lookup"><span data-stu-id="86254-116">Detailed information about the tablet context to create.</span></span>

</dd> <dt>

<span data-ttu-id="86254-117">*CET* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86254-117">*cet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86254-118">Valor que habilita ou desabilita as mensagens de contexto que estão sendo enviadas para a janela.</span><span class="sxs-lookup"><span data-stu-id="86254-118">Value that enables or disables context messages being sent to the window.</span></span>

</dd> <dt>

<span data-ttu-id="86254-119">*ppCtx* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="86254-119">*ppCtx* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86254-120">Um ponteiro para o novo contexto do Tablet.</span><span class="sxs-lookup"><span data-stu-id="86254-120">A pointer to the newly create tablet context.</span></span>

</dd> <dt>

<span data-ttu-id="86254-121">*pTcid* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="86254-121">*pTcid* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="86254-122">Valor que identifica exclusivamente o Tablet.</span><span class="sxs-lookup"><span data-stu-id="86254-122">Value that uniquely identifies the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="86254-123">*ppPD* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="86254-123">*ppPD* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="86254-124">Ponteiro para informações sobre quais dados estão contidos em cada pacote.</span><span class="sxs-lookup"><span data-stu-id="86254-124">Pointer to information about what data is contained in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="86254-125">*pSink* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86254-125">*pSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86254-126">O objeto [**ITabletEventSink**](itableteventsink.md) em que as mensagens de notificação serão enviadas.</span><span class="sxs-lookup"><span data-stu-id="86254-126">The [**ITabletEventSink**](itableteventsink.md) object where notification messages will be sent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86254-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="86254-127">Return value</span></span>

<span data-ttu-id="86254-128">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="86254-128">This method can return one of these values.</span></span>



| <span data-ttu-id="86254-129">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="86254-129">Return code</span></span>                                                                            | <span data-ttu-id="86254-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="86254-130">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="86254-131"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="86254-131"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="86254-132">Êxito.</span><span class="sxs-lookup"><span data-stu-id="86254-132">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="86254-133"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="86254-133"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="86254-134">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="86254-134">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="86254-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="86254-135">Remarks</span></span>

<span data-ttu-id="86254-136">Normalmente, um aplicativo obtém os valores padrão do [**método ITablet:: GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifica os valores para atender às suas necessidades e, em seguida, passa a estrutura de configurações modificada para o **método ITablet:: CreateContext**.</span><span class="sxs-lookup"><span data-stu-id="86254-136">Typically, an application obtains the default values from the [**ITablet::GetDefaultContextSettings Method**](itablet-getdefaultcontextsettings.md), modifies values to suit their needs, and then passes the modified settings structure to the **ITablet::CreateContext Method**.</span></span>

> [!Note]  
> <span data-ttu-id="86254-137">Você deve implementar a [**interface ITabletEventSink**](itableteventsink.md) ao chamar o **método ITablet:: CreateContext**.</span><span class="sxs-lookup"><span data-stu-id="86254-137">You must implement the [**ITabletEventSink Interface**](itableteventsink.md) when calling the **ITablet::CreateContext Method**.</span></span>

 

<span data-ttu-id="86254-138">O parâmetro *dwOptions* é um conjunto de sinalizadores de bits que descrevem as opções de contexto.</span><span class="sxs-lookup"><span data-stu-id="86254-138">The *dwOptions* parameter is a set of bit flags that describe context options.</span></span> <span data-ttu-id="86254-139">A tabela a seguir descreve esses sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="86254-139">The following table describes these flags.</span></span>



| <span data-ttu-id="86254-140">Nome do sinalizador</span><span class="sxs-lookup"><span data-stu-id="86254-140">Flag Name</span></span>                                | <span data-ttu-id="86254-141">Valor</span><span class="sxs-lookup"><span data-stu-id="86254-141">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="86254-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="86254-142">Description</span></span>                                                                                                                                                                                                                                                              |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86254-143">margem de TCXO \_</span><span class="sxs-lookup"><span data-stu-id="86254-143">TCXO\_MARGIN</span></span><br/>                  | <span data-ttu-id="86254-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="86254-144">0x00000001</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="86254-145">Especifica que o contexto de entrada no Tablet terá uma margem.</span><span class="sxs-lookup"><span data-stu-id="86254-145">Specifies that the input context on the tablet will have a margin.</span></span> <span data-ttu-id="86254-146">A margem é uma área fora da área de entrada especificada, na qual os eventos serão mapeados para a borda da área de entrada.</span><span class="sxs-lookup"><span data-stu-id="86254-146">The margin is an area outside the specified input area where events will be mapped to the edge of the input area.</span></span> <span data-ttu-id="86254-147">Esse recurso facilita a entrada de pontos na borda do contexto.</span><span class="sxs-lookup"><span data-stu-id="86254-147">This feature makes it easier to input points at the edge of the context.</span></span><br/> |
| <span data-ttu-id="86254-148">prehook TCXO \_</span><span class="sxs-lookup"><span data-stu-id="86254-148">TCXO\_PREHOOK</span></span><br/>                 | <span data-ttu-id="86254-149">0x00000002</span><span class="sxs-lookup"><span data-stu-id="86254-149">0x00000002</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="86254-150">O prehook Obtém pacotes antes de contextos e de conganchos regulares.</span><span class="sxs-lookup"><span data-stu-id="86254-150">Prehook gets packets before regular contexts and posthooks.</span></span> <span data-ttu-id="86254-151">Eles obtêm pacotes na ordem de sua criação.</span><span class="sxs-lookup"><span data-stu-id="86254-151">They get packets in the order of their creation.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="86254-152">\_estado do cursor TCXO \_</span><span class="sxs-lookup"><span data-stu-id="86254-152">TCXO\_CURSOR\_STATE</span></span><br/>           | <span data-ttu-id="86254-153">0x00000004</span><span class="sxs-lookup"><span data-stu-id="86254-153">0x00000004</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="86254-154">O TC retornará pacotes, mesmo se o cursor estiver ativo.</span><span class="sxs-lookup"><span data-stu-id="86254-154">The TC will return packets even if the cursor is up.</span></span> <span data-ttu-id="86254-155">Por padrão, um TC retornará apenas os pacotes quando o cursor estiver inativo.</span><span class="sxs-lookup"><span data-stu-id="86254-155">By default, a TC will only return packets when the cursor is down.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="86254-156">TCXO \_ sem \_ cursor \_</span><span class="sxs-lookup"><span data-stu-id="86254-156">TCXO\_NO\_CURSOR\_DOWN</span></span><br/>        | <span data-ttu-id="86254-157">0x00000008</span><span class="sxs-lookup"><span data-stu-id="86254-157">0x00000008</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="86254-158">O TC não retornará pacotes quando o cursor estiver inativo.</span><span class="sxs-lookup"><span data-stu-id="86254-158">The TC will not return packets when the cursor is down.</span></span><br/>                                                                                                                                                                                                       |
| <span data-ttu-id="86254-159">TCXO \_ não \_ integrado</span><span class="sxs-lookup"><span data-stu-id="86254-159">TCXO\_NON\_INTEGRATED</span></span><br/>         | <span data-ttu-id="86254-160">0x00000010</span><span class="sxs-lookup"><span data-stu-id="86254-160">0x00000010</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="86254-161">O contexto será não integrado.</span><span class="sxs-lookup"><span data-stu-id="86254-161">The context will be non-integrated.</span></span><br/>                                                                                                                                                                                                                           |
| <span data-ttu-id="86254-162">TCXO \_</span><span class="sxs-lookup"><span data-stu-id="86254-162">TCXO\_POSTHOOK</span></span><br/>                | <span data-ttu-id="86254-163">0x00000020</span><span class="sxs-lookup"><span data-stu-id="86254-163">0x00000020</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="86254-164">O createhook Obtém pacotes após contextos de Tablet regulares, mas antes do contexto do sistema.</span><span class="sxs-lookup"><span data-stu-id="86254-164">Posthooks get packets after regular tablet contexts but before the system context.</span></span> <span data-ttu-id="86254-165">Eles obtêm pacotes na ordem inversa de sua criação.</span><span class="sxs-lookup"><span data-stu-id="86254-165">They get packets in the reverse order of their creation.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="86254-166">TCXO \_ não \_ Mostrar \_ cursor</span><span class="sxs-lookup"><span data-stu-id="86254-166">TCXO\_DONT\_SHOW\_CURSOR</span></span><br/>      | <span data-ttu-id="86254-167">0x00000080</span><span class="sxs-lookup"><span data-stu-id="86254-167">0x00000080</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="86254-168">O TC não definirá a posição do cursor.</span><span class="sxs-lookup"><span data-stu-id="86254-168">The TC will not set the cursor position.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="86254-169">TCXO \_ não \_ validar \_ TCS</span><span class="sxs-lookup"><span data-stu-id="86254-169">TCXO\_DONT\_VALIDATE\_TCS</span></span><br/>     | <span data-ttu-id="86254-170">0x00000100</span><span class="sxs-lookup"><span data-stu-id="86254-170">0x00000100</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="86254-171">O TC não validará os GUIDs passados nas configurações de contexto do Tablet nas propriedades com suporte do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="86254-171">The TC will not validate the GUIDS passed in the tablet context settings against the supported properties of the device.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="86254-172">TCXO \_ permitir \_ movimentos</span><span class="sxs-lookup"><span data-stu-id="86254-172">TCXO\_ALLOW\_FLICKS</span></span><br/>           | <span data-ttu-id="86254-173">0x00000400</span><span class="sxs-lookup"><span data-stu-id="86254-173">0x00000400</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="86254-174">O TC permitirá que a detecção de movimento ocorra (por padrão, isso só é permitido em contextos do sistema) e o cliente receberá \_ eventos de movimento.</span><span class="sxs-lookup"><span data-stu-id="86254-174">The TC will allow flick detection to take place (by default this is only allowed on system contexts), and the client will get SE\_FLICK events.</span></span><br/>                                                                                                               |
| <span data-ttu-id="86254-175">TCXO \_ permitir \_ toques de comentários \_</span><span class="sxs-lookup"><span data-stu-id="86254-175">TCXO\_ALLOW\_FEEDBACK\_TAPS</span></span><br/>   | <span data-ttu-id="86254-176">0x00000800</span><span class="sxs-lookup"><span data-stu-id="86254-176">0x00000800</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="86254-177">O TC permitirá que os comentários da caneta sejam mostrados.</span><span class="sxs-lookup"><span data-stu-id="86254-177">The TC will allow pen feedback to be shown.</span></span> <span data-ttu-id="86254-178">Por padrão, isso só é permitido em contextos do sistema.</span><span class="sxs-lookup"><span data-stu-id="86254-178">By default, this is only allowed on system contexts.</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="86254-179">TCXO \_ permitir \_ \_ desroscar comentários</span><span class="sxs-lookup"><span data-stu-id="86254-179">TCXO\_ALLOW\_FEEDBACK\_BARREL</span></span><br/> | <span data-ttu-id="86254-180">0x00001000</span><span class="sxs-lookup"><span data-stu-id="86254-180">0x00001000</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="86254-181">O TC permitirá que os comentários da caneta sejam mostrados.</span><span class="sxs-lookup"><span data-stu-id="86254-181">The TC will allow pen feedback to be shown.</span></span> <span data-ttu-id="86254-182">Por padrão, isso só é permitido em contextos do sistema.</span><span class="sxs-lookup"><span data-stu-id="86254-182">By default, this is only allowed on system contexts.</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="86254-183">TCXO \_ tudo</span><span class="sxs-lookup"><span data-stu-id="86254-183">TCXO\_ALL</span></span><br/>                     | <span data-ttu-id="86254-184">TCXO \_ Margin \| TCXO pré- \_ gancho \| TCXO \_ estado do cursor \_ \| TCXO \_ não há \_ cursor \_ para baixo \| TCXO não integrado TCXO pré-Hook TCXO \_ não \_ \| \_ \| \_ \_ Mostrar \_ cursor TCXO não \| \_ \_ validar \_ TCS</span><span class="sxs-lookup"><span data-stu-id="86254-184">TCXO\_MARGIN \| TCXO\_PREHOOK \| TCXO\_CURSOR\_STATE \| TCXO\_NO\_CURSOR\_DOWN \| TCXO\_NON\_INTEGRATED \| TCXO\_POSTHOOK \| TCXO\_DONT\_SHOW\_CURSOR \| TCXO\_DONT\_VALIDATE\_TCS</span></span><br/> | <span data-ttu-id="86254-185">Todas as opções de contexto do Tablet definidas.</span><span class="sxs-lookup"><span data-stu-id="86254-185">All defined tablet context options.</span></span><br/>                                                                                                                                                                                                                           |
| <span data-ttu-id="86254-186">gancho de TCXO \_</span><span class="sxs-lookup"><span data-stu-id="86254-186">TCXO\_HOOK</span></span><br/>                    | <span data-ttu-id="86254-187">TCXO de TCXO de prehook \_ \| \_</span><span class="sxs-lookup"><span data-stu-id="86254-187">TCXO\_PREHOOK \| TCXO\_POSTHOOK</span></span><br/>                                                                                                                                                    | <span data-ttu-id="86254-188">Combina a funcionalidade de pré e pós-gancho.</span><span class="sxs-lookup"><span data-stu-id="86254-188">Combines pre-hook and post-hook functionality.</span></span><br/>                                                                                                                                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="86254-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86254-189">Requirements</span></span>



| <span data-ttu-id="86254-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="86254-190">Requirement</span></span> | <span data-ttu-id="86254-191">Valor</span><span class="sxs-lookup"><span data-stu-id="86254-191">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86254-192">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86254-192">Minimum supported client</span></span><br/> | <span data-ttu-id="86254-193">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="86254-193">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="86254-194">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86254-194">Minimum supported server</span></span><br/> | <span data-ttu-id="86254-195">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="86254-195">None supported</span></span><br/>                                                              |
| <span data-ttu-id="86254-196">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86254-196">Library</span></span><br/>                  | <dl> <span data-ttu-id="86254-197"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="86254-197"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86254-198">Confira também</span><span class="sxs-lookup"><span data-stu-id="86254-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86254-199">**Interface ITablet**</span><span class="sxs-lookup"><span data-stu-id="86254-199">**ITablet Interface**</span></span>](itablet.md)
</dt> <dt>

[<span data-ttu-id="86254-200">**\_Enumeração de tipo de habilitação de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="86254-200">**CONTEXT\_ENABLE\_TYPE Enumeration**</span></span>](context-enable-type.md)
</dt> <dt>

[<span data-ttu-id="86254-201">**Estrutura de configurações de \_ contexto do Tablet \_**</span><span class="sxs-lookup"><span data-stu-id="86254-201">**TABLET\_CONTEXT\_SETTINGS Structure**</span></span>](tablet-context-settings.md)
</dt> <dt>

[<span data-ttu-id="86254-202">**Estrutura de descrição do pacote \_**</span><span class="sxs-lookup"><span data-stu-id="86254-202">**PACKET\_DESCRIPTION Structure**</span></span>](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)
</dt> <dt>

[<span data-ttu-id="86254-203">**Interface ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="86254-203">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> <dt>

[<span data-ttu-id="86254-204">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="86254-204">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 





---
description: Recupera as opções associadas a um compartilhamento DDE que está na lista de compartilhamentos confiáveis dos usuários do servidor.
ms.assetid: e5f2b4f8-f922-4734-9fe3-8a74a7f5f619
title: Função NDdeGetTrustedShare (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetTrustedShare
- NDdeGetTrustedShareA
- NDdeGetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 1f8d7e79c48e0409d8040f6d44159c473dd58ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787557"
---
# <a name="nddegettrustedshare-function"></a><span data-ttu-id="7b1b5-103">Função NDdeGetTrustedShare</span><span class="sxs-lookup"><span data-stu-id="7b1b5-103">NDdeGetTrustedShare function</span></span>

<span data-ttu-id="7b1b5-104">\[Não há mais suporte para DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="7b1b5-105">Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="7b1b5-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="7b1b5-106">Recupera as opções associadas a um compartilhamento DDE que está na lista de compartilhamentos confiáveis do usuário do servidor.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-106">Retrieves the options associated with a DDE share that is in the server user's list of trusted shares.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b1b5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b1b5-107">Syntax</span></span>


```C++
UINT NDdeGetTrustedShare(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _Out_ LPDWORD lpdwTrustOptions,
  _Out_ LPDWORD lpdwShareModId0,
  _Out_ LPDWORD lpdwShareModId1
);
```



## <a name="parameters"></a><span data-ttu-id="7b1b5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b1b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b1b5-109">*lpszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b1b5-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b1b5-110">O nome do servidor no qual o DSDM reside.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-110">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="7b1b5-111">*lpszShareName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b1b5-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b1b5-112">O nome do compartilhamento cujo status confiável está sendo consultado.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-112">The share name whose trusted status is being queried.</span></span> <span data-ttu-id="7b1b5-113">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7b1b5-114">*lpdwTrustOptions* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7b1b5-114">*lpdwTrustOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b1b5-115">Um ponteiro para uma variável que recebe as opções de confiança.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-115">A pointer to a variable that receives the trust options.</span></span> <span data-ttu-id="7b1b5-116">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-116">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="7b1b5-117">As opções de confiança a seguir estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-117">The following trust options are available.</span></span>



| <span data-ttu-id="7b1b5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7b1b5-118">Value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="7b1b5-119">Significado</span><span class="sxs-lookup"><span data-stu-id="7b1b5-119">Meaning</span></span>                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <span data-ttu-id="7b1b5-120"><dt>**NDDE \_ CMD \_ Mostrar \_ máscara**</dt> <dt>0x0000FFFFL</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-120"><dt>**NDDE\_CMD\_SHOW\_MASK**</dt> <dt>0x0000FFFFL</dt></span></span> </dl>             | <span data-ttu-id="7b1b5-121">Máscara usada para obter o valor usado para substituir o estado de exibição do compartilhamento DDE, se NDDE \_ Trust \_ cmd \_ show estiver definido.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-121">Mask used to obtain the value used to override the DDE share show state, if NDDE\_TRUST\_CMD\_SHOW is set.</span></span><br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <span data-ttu-id="7b1b5-122"><dt>**NDDE \_ TRUST \_ cmd \_ show**</dt> <dt>0x10000000L</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-122"><dt>**NDDE\_TRUST\_CMD\_SHOW**</dt> <dt>0x10000000L</dt></span></span> </dl>          | <span data-ttu-id="7b1b5-123">Substitua o estado de exibição especificado no DSDM de compartilhamento DDE.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-123">Override the show state specified in the DDE share DSDM.</span></span><br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <span data-ttu-id="7b1b5-124"><dt>**NDDE \_ CONFIAR no \_ compartilhamento \_ del**</dt> <dt>0x20000000L</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-124"><dt>**NDDE\_TRUST\_SHARE\_DEL**</dt> <dt>0x20000000L</dt></span></span> </dl>       | <span data-ttu-id="7b1b5-125">Remova o status confiável do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-125">Remove the share's trusted status.</span></span><br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <span data-ttu-id="7b1b5-126"><dt>**NDDE \_ 0x40000000L \_ de \_ inicialização de compartilhamento de confiança**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-126"><dt>**NDDE\_TRUST\_SHARE\_INIT**</dt> <dt>0x40000000L</dt></span></span> </dl>    | <span data-ttu-id="7b1b5-127">Permitir que um cliente inicie para o aplicativo se ele já estiver em execução no contexto do usuário.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-127">Allow a client to initiate to the application if it is already running in the user's context.</span></span><br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <span data-ttu-id="7b1b5-128"><dt>**NDDE \_ CONFIAR \_ no \_ início do compartilhamento**</dt> <dt>0x80000000L</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-128"><dt>**NDDE\_TRUST\_SHARE\_START**</dt> <dt>0x80000000L</dt></span></span> </dl> | <span data-ttu-id="7b1b5-129">Permitir que o aplicativo seja iniciado no contexto do usuário.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-129">Allow the application to be started in the user's context.</span></span><br/>                                                 |



 

</dd> <dt>

<span data-ttu-id="7b1b5-130">*lpdwShareModId0* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7b1b5-130">*lpdwShareModId0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b1b5-131">Um ponteiro para uma variável que recebe a primeira parte do identificador de modificação de compartilhamento confiável.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-131">A pointer to a variable that receives the first part of the trusted share modify identifier.</span></span> <span data-ttu-id="7b1b5-132">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-132">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7b1b5-133">*lpdwShareModId1* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7b1b5-133">*lpdwShareModId1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b1b5-134">Um ponteiro para uma variável que recebe a segunda parte do identificador de modificação de compartilhamento confiável.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-134">A pointer to a variable that receives the second part of the trusted share modify identifier.</span></span> <span data-ttu-id="7b1b5-135">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-135">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b1b5-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b1b5-136">Return value</span></span>

<span data-ttu-id="7b1b5-137">Se a função for realizada com sucesso, o valor de retorno será NDDE \_ nenhum \_ erro.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-137">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="7b1b5-138">Se a função falhar, o valor de retorno será um código de erro, que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="7b1b5-138">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7b1b5-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b1b5-139">Remarks</span></span>

<span data-ttu-id="7b1b5-140">O identificador de modificação de compartilhamento confiável reflete a versão do compartilhamento DDE no DSDM no momento em que o compartilhamento de DDE recebeu inicialmente o status confiável.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-140">The trusted share modify identifier reflects the version of the DDE share in the DSDM at the time the DDE share was initially granted trusted status.</span></span> <span data-ttu-id="7b1b5-141">O identificador de modificação de compartilhamento confiável é usado principalmente para remover compartilhamentos confiáveis obsoletos.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-141">The trusted share modify identifier is primarily used to remove obsolete trusted shares.</span></span> <span data-ttu-id="7b1b5-142">No entanto, o usuário não precisa remover compartilhamentos confiáveis obsoletos.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-142">However, the user does not need to remove obsolete trusted shares.</span></span> <span data-ttu-id="7b1b5-143">O agente DDE de rede remove compartilhamentos obsoletos em nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-143">The network DDE agent removes obsolete shares on the user's behalf.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b1b5-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b1b5-144">Requirements</span></span>



| <span data-ttu-id="7b1b5-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b1b5-145">Requirement</span></span> | <span data-ttu-id="7b1b5-146">Valor</span><span class="sxs-lookup"><span data-stu-id="7b1b5-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b1b5-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b1b5-147">Minimum supported client</span></span><br/> | <span data-ttu-id="7b1b5-148">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7b1b5-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7b1b5-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b1b5-149">Minimum supported server</span></span><br/> | <span data-ttu-id="7b1b5-150">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7b1b5-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7b1b5-151">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7b1b5-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b1b5-152"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-152"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="7b1b5-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b1b5-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="7b1b5-154"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-154"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7b1b5-155">DLL</span><span class="sxs-lookup"><span data-stu-id="7b1b5-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b1b5-156"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-156"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="7b1b5-157">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="7b1b5-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7b1b5-158">**NDdeGetTrustedShareW** (Unicode) e **NDdeGetTrustedShareA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7b1b5-158">**NDdeGetTrustedShareW** (Unicode) and **NDdeGetTrustedShareA** (ANSI)</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="7b1b5-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b1b5-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b1b5-160">Visão geral de troca dinâmica de dados de rede</span><span class="sxs-lookup"><span data-stu-id="7b1b5-160">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="7b1b5-161">Funções DDE de rede</span><span class="sxs-lookup"><span data-stu-id="7b1b5-161">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="7b1b5-162">**NDdeSetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="7b1b5-162">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)
</dt> </dl>

 

 





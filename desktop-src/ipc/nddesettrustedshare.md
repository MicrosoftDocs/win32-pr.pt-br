---
description: Concede o status confiável do compartilhamento DDE especificado dentro do contexto de usuários atual.
ms.assetid: 508d3603-468c-4ecb-8e5c-0ab86c2ff3b4
title: Função NDdeSetTrustedShare (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetTrustedShare
- NDdeSetTrustedShareA
- NDdeSetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 459e1621848e212522064ff6f01316fc23183bc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501289"
---
# <a name="nddesettrustedshare-function"></a><span data-ttu-id="a0f6f-103">Função NDdeSetTrustedShare</span><span class="sxs-lookup"><span data-stu-id="a0f6f-103">NDdeSetTrustedShare function</span></span>

<span data-ttu-id="a0f6f-104">\[Não há mais suporte para DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="a0f6f-105">Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="a0f6f-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="a0f6f-106">Concede o status confiável do compartilhamento DDE especificado no contexto do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-106">Grants the specified DDE share trusted status within the current user's context.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0f6f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0f6f-107">Syntax</span></span>


```C++
UINT NDdeSetTrustedShare(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ DWORD  dwTrustOptions
);
```



## <a name="parameters"></a><span data-ttu-id="a0f6f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0f6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0f6f-109">*lpszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0f6f-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f6f-110">O nome do servidor cujo DSDM deve ser modificado.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="a0f6f-111">*lpszShareName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0f6f-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f6f-112">O nome do compartilhamento para o qual receber o status confiável.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-112">The name of the share to be granted trusted status.</span></span> <span data-ttu-id="a0f6f-113">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a0f6f-114">*dwTrustOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0f6f-114">*dwTrustOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f6f-115">As opções que afetam o status confiável do compartilhamento DDE.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-115">The options affecting the trusted status of the DDE share.</span></span> <span data-ttu-id="a0f6f-116">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a0f6f-117">Opção</span><span class="sxs-lookup"><span data-stu-id="a0f6f-117">Option</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="a0f6f-118">Significado</span><span class="sxs-lookup"><span data-stu-id="a0f6f-118">Meaning</span></span>                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <span data-ttu-id="a0f6f-119"><dt>**NDDE \_ CMD \_ Mostrar \_ máscara**</dt> <dt>0x0000FFFFL</dt></span><span class="sxs-lookup"><span data-stu-id="a0f6f-119"><dt>**NDDE\_CMD\_SHOW\_MASK**</dt> <dt>0x0000FFFFL</dt></span></span> </dl>             | <span data-ttu-id="a0f6f-120">Máscara usada para obter o valor usado para substituir o estado de exibição do compartilhamento DDE, se NDDE \_ Trust \_ cmd \_ show estiver definido.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-120">Mask used to obtain the value used to override the DDE share show state, if NDDE\_TRUST\_CMD\_SHOW is set.</span></span><br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <span data-ttu-id="a0f6f-121"><dt>**NDDE \_ TRUST \_ cmd \_ show**</dt> <dt>0x10000000L</dt></span><span class="sxs-lookup"><span data-stu-id="a0f6f-121"><dt>**NDDE\_TRUST\_CMD\_SHOW**</dt> <dt>0x10000000L</dt></span></span> </dl>          | <span data-ttu-id="a0f6f-122">Substitua o estado de exibição especificado no DSDM de compartilhamento DDE.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-122">Override the show state specified in the DDE share DSDM.</span></span><br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <span data-ttu-id="a0f6f-123"><dt>**NDDE \_ CONFIAR no \_ compartilhamento \_ del**</dt> <dt>0x20000000L</dt></span><span class="sxs-lookup"><span data-stu-id="a0f6f-123"><dt>**NDDE\_TRUST\_SHARE\_DEL**</dt> <dt>0x20000000L</dt></span></span> </dl>       | <span data-ttu-id="a0f6f-124">Remova o status confiável do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-124">Remove the share's trusted status.</span></span><br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <span data-ttu-id="a0f6f-125"><dt>**NDDE \_ 0x40000000L \_ de \_ inicialização de compartilhamento de confiança**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a0f6f-125"><dt>**NDDE\_TRUST\_SHARE\_INIT**</dt> <dt>0x40000000L</dt></span></span> </dl>    | <span data-ttu-id="a0f6f-126">Permitir que um cliente inicie para o aplicativo se ele já estiver em execução no contexto do usuário.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-126">Allow a client to initiate to the application if it is already running in the user's context.</span></span><br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <span data-ttu-id="a0f6f-127"><dt>**NDDE \_ CONFIAR \_ no \_ início do compartilhamento**</dt> <dt>0x80000000L</dt></span><span class="sxs-lookup"><span data-stu-id="a0f6f-127"><dt>**NDDE\_TRUST\_SHARE\_START**</dt> <dt>0x80000000L</dt></span></span> </dl> | <span data-ttu-id="a0f6f-128">Permitir que o aplicativo seja iniciado no contexto do usuário.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-128">Allow the application to be started in the user's context.</span></span><br/>                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0f6f-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a0f6f-129">Return value</span></span>

<span data-ttu-id="a0f6f-130">Se a função for realizada com sucesso, o valor de retorno será NDDE \_ nenhum \_ erro.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-130">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="a0f6f-131">Se a função falhar, o valor de retorno será um código de erro, que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="a0f6f-131">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a0f6f-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0f6f-132">Remarks</span></span>

<span data-ttu-id="a0f6f-133">O compartilhamento DDE deve ser criado primeiro com [**NDdeShareAdd**](nddeshareadd.md).</span><span class="sxs-lookup"><span data-stu-id="a0f6f-133">The DDE share must first be created with [**NDdeShareAdd**](nddeshareadd.md).</span></span>

<span data-ttu-id="a0f6f-134">Se **NDdeSetTrustedShare** for chamado com *dwTrustOptions* definido como zero, o compartilhamento confiável perderá seu status confiável.</span><span class="sxs-lookup"><span data-stu-id="a0f6f-134">If **NDdeSetTrustedShare** is called with *dwTrustOptions* set to zero, the trusted share loses its trusted status.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0f6f-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0f6f-135">Requirements</span></span>



| <span data-ttu-id="a0f6f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0f6f-136">Requirement</span></span> | <span data-ttu-id="a0f6f-137">Valor</span><span class="sxs-lookup"><span data-stu-id="a0f6f-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f6f-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0f6f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a0f6f-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a0f6f-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a0f6f-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0f6f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a0f6f-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a0f6f-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a0f6f-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a0f6f-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0f6f-143"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0f6f-143"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0f6f-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0f6f-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="a0f6f-145"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0f6f-145"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a0f6f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="a0f6f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0f6f-147"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0f6f-147"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="a0f6f-148">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="a0f6f-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a0f6f-149">**NDdeSetTrustedShareW** (Unicode) e **NDdeSetTrustedShareA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a0f6f-149">**NDdeSetTrustedShareW** (Unicode) and **NDdeSetTrustedShareA** (ANSI)</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="a0f6f-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0f6f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0f6f-151">Visão geral de troca dinâmica de dados de rede</span><span class="sxs-lookup"><span data-stu-id="a0f6f-151">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="a0f6f-152">Funções DDE de rede</span><span class="sxs-lookup"><span data-stu-id="a0f6f-152">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="a0f6f-153">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="a0f6f-153">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 





---
description: Cria e adiciona um novo compartilhamento DDE ao Gerenciador de banco de dados de compartilhamento DDE (DSDM).
ms.assetid: c9814919-412e-4f13-98cc-373b69545734
title: Função NDdeShareAdd (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareAdd
- NDdeShareAddA
- NDdeShareAddW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 282ff7ed3e1564044591966fb4233b2eda1d3227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789524"
---
# <a name="nddeshareadd-function"></a><span data-ttu-id="03ce2-103">Função NDdeShareAdd</span><span class="sxs-lookup"><span data-stu-id="03ce2-103">NDdeShareAdd function</span></span>

<span data-ttu-id="03ce2-104">\[Não há mais suporte para DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="03ce2-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="03ce2-105">Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="03ce2-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="03ce2-106">Cria e adiciona um novo compartilhamento DDE ao Gerenciador de banco de dados de compartilhamento DDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="03ce2-106">Creates and adds a new DDE share to the DDE share database manager (DSDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="03ce2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03ce2-107">Syntax</span></span>


```C++
UINT NDdeShareAdd(
  _In_ LPTSTR               lpszServer,
  _In_ UINT                 nLevel,
  _In_ PSECURITY_DESCRIPTOR pSD,
  _In_ LPBYTE               lpBuffer,
  _In_ DWORD                cBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="03ce2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03ce2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03ce2-109">*lpszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="03ce2-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ce2-110">O nome do servidor cujo DSDM deve ser modificado.</span><span class="sxs-lookup"><span data-stu-id="03ce2-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="03ce2-111">*nLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="03ce2-111">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ce2-112">O nível de informações.</span><span class="sxs-lookup"><span data-stu-id="03ce2-112">The information level.</span></span> <span data-ttu-id="03ce2-113">Esse parâmetro deve ser 2.</span><span class="sxs-lookup"><span data-stu-id="03ce2-113">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="03ce2-114">*PSD* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="03ce2-114">*pSD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ce2-115">Um ponteiro para uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) a ser associado a esse compartilhamento e no qual as verificações de acesso serão executadas em logons subsequentes para esse compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="03ce2-115">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure to be associated with this share and against which access checks will be performed on subsequent initiates to this share.</span></span> <span data-ttu-id="03ce2-116">Esse parâmetro pode ser **nulo** e, nesse caso, o DSDM cria um descritor de segurança padrão que concede "controle total" ao proprietário e "ler e vincular" a todos.</span><span class="sxs-lookup"><span data-stu-id="03ce2-116">This parameter can be **NULL**, in which case the DSDM creates a default security descriptor that grants "Full Control" to the owner and "Read and Link" to everyone.</span></span>

</dd> <dt>

<span data-ttu-id="03ce2-117">*lpBuffer* \[in\]</span><span class="sxs-lookup"><span data-stu-id="03ce2-117">*lpBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ce2-118">Um ponteiro para a estrutura [**NDDESHAREINFO**](nddeshareinfo-str.md) que define a lista ApplicationTopic associada ao compartilhamento DDE que está sendo criado, bem como outros parâmetros.</span><span class="sxs-lookup"><span data-stu-id="03ce2-118">A pointer to the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure that defines the ApplicationTopic list associated with the DDE share being created as well as other parameters.</span></span> <span data-ttu-id="03ce2-119">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="03ce2-119">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="03ce2-120">*cBufSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="03ce2-120">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ce2-121">O tamanho da estrutura *lpBuffer* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="03ce2-121">The size of the *lpBuffer* structure, in bytes.</span></span> <span data-ttu-id="03ce2-122">Este parâmetro não pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="03ce2-122">This parameter cannot be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03ce2-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="03ce2-123">Return value</span></span>

<span data-ttu-id="03ce2-124">Se a função for realizada com sucesso, o valor de retorno será NDDE \_ nenhum \_ erro.</span><span class="sxs-lookup"><span data-stu-id="03ce2-124">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="03ce2-125">Se a função falhar, o valor de retorno será um código de erro, que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="03ce2-125">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="03ce2-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="03ce2-126">Remarks</span></span>

<span data-ttu-id="03ce2-127">Antes que um cliente possa se conectar ao compartilhamento de DDE, ele deve ser confiável com [**NDdeSetTrustedShare**](nddesettrustedshare.md).</span><span class="sxs-lookup"><span data-stu-id="03ce2-127">Before a client can connect to the DDE share, it must be trusted with [**NDdeSetTrustedShare**](nddesettrustedshare.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03ce2-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03ce2-128">Requirements</span></span>



| <span data-ttu-id="03ce2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="03ce2-129">Requirement</span></span> | <span data-ttu-id="03ce2-130">Valor</span><span class="sxs-lookup"><span data-stu-id="03ce2-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03ce2-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03ce2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="03ce2-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="03ce2-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="03ce2-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03ce2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="03ce2-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="03ce2-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="03ce2-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="03ce2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="03ce2-136"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="03ce2-136"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="03ce2-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="03ce2-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="03ce2-138"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03ce2-138"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="03ce2-139">DLL</span><span class="sxs-lookup"><span data-stu-id="03ce2-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03ce2-140"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03ce2-140"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="03ce2-141">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="03ce2-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="03ce2-142">**NDdeShareAddW** (Unicode) e **NDdeShareAddA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="03ce2-142">**NDdeShareAddW** (Unicode) and **NDdeShareAddA** (ANSI)</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="03ce2-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="03ce2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03ce2-144">Visão geral de troca dinâmica de dados de rede</span><span class="sxs-lookup"><span data-stu-id="03ce2-144">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="03ce2-145">Funções DDE de rede</span><span class="sxs-lookup"><span data-stu-id="03ce2-145">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="03ce2-146">**NDDESHAREINFO**</span><span class="sxs-lookup"><span data-stu-id="03ce2-146">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="03ce2-147">**NDdeSetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="03ce2-147">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)
</dt> </dl>

 


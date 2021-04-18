---
description: Exclui um compartilhamento DDE do DSDM (Gerenciador de banco de dados de compartilhamento) DDE.
ms.assetid: 3240f4b1-2625-46bc-9bbe-27737c59df81
title: Função NDdeShareDel (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareDel
- NDdeShareDelA
- NDdeShareDelW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 2d57307c157c532e124699b6bfb2ed666f374722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760053"
---
# <a name="nddesharedel-function"></a><span data-ttu-id="56557-103">Função NDdeShareDel</span><span class="sxs-lookup"><span data-stu-id="56557-103">NDdeShareDel function</span></span>

<span data-ttu-id="56557-104">\[Não há mais suporte para DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="56557-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="56557-105">Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="56557-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="56557-106">Exclui um compartilhamento DDE do DSDM (Gerenciador de banco de dados de compartilhamento) DDE.</span><span class="sxs-lookup"><span data-stu-id="56557-106">Deletes a DDE share from the DDE share database manager (DSDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="56557-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56557-107">Syntax</span></span>


```C++
UINT NDdeShareDel(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   wReserved
);
```



## <a name="parameters"></a><span data-ttu-id="56557-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56557-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56557-109">*lpszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="56557-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56557-110">O nome do servidor cujo DSDM deve ser modificado.</span><span class="sxs-lookup"><span data-stu-id="56557-110">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="56557-111">*lpszShareName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="56557-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56557-112">O nome do compartilhamento a ser excluído do DSDM.</span><span class="sxs-lookup"><span data-stu-id="56557-112">The name of the share to be deleted from the DSDM.</span></span> <span data-ttu-id="56557-113">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="56557-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="56557-114">*wReserved* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="56557-114">*wReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56557-115">Reservado.</span><span class="sxs-lookup"><span data-stu-id="56557-115">Reserved.</span></span> <span data-ttu-id="56557-116">Esse parâmetro deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="56557-116">This parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56557-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56557-117">Return value</span></span>

<span data-ttu-id="56557-118">Se a função for realizada com sucesso, o valor de retorno será NDDE \_ nenhum \_ erro.</span><span class="sxs-lookup"><span data-stu-id="56557-118">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="56557-119">Se a função falhar, o valor de retorno será um código de erro que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="56557-119">If the function fails, the return value is an error code which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="56557-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="56557-120">Remarks</span></span>

<span data-ttu-id="56557-121">Para excluir um compartilhamento DDE do DSDM, você deve ter o privilégio apropriado.</span><span class="sxs-lookup"><span data-stu-id="56557-121">To delete a DDE share from the DSDM, you must have the appropriate privilege.</span></span> <span data-ttu-id="56557-122">O criador de compartilhamento tem o privilégio de exclusão.</span><span class="sxs-lookup"><span data-stu-id="56557-122">The share creator has delete privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="56557-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56557-123">Requirements</span></span>



| <span data-ttu-id="56557-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="56557-124">Requirement</span></span> | <span data-ttu-id="56557-125">Valor</span><span class="sxs-lookup"><span data-stu-id="56557-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56557-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56557-126">Minimum supported client</span></span><br/> | <span data-ttu-id="56557-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="56557-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="56557-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56557-128">Minimum supported server</span></span><br/> | <span data-ttu-id="56557-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="56557-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="56557-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="56557-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="56557-131"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="56557-131"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="56557-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="56557-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="56557-133"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56557-133"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="56557-134">DLL</span><span class="sxs-lookup"><span data-stu-id="56557-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56557-135"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56557-135"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="56557-136">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="56557-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="56557-137">**NDdeShareDelW** (Unicode) e **NDdeShareDelA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="56557-137">**NDdeShareDelW** (Unicode) and **NDdeShareDelA** (ANSI)</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="56557-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="56557-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56557-139">Visão geral de troca dinâmica de dados de rede</span><span class="sxs-lookup"><span data-stu-id="56557-139">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="56557-140">Funções DDE de rede</span><span class="sxs-lookup"><span data-stu-id="56557-140">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 





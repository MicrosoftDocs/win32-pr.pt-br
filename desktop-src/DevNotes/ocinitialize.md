---
description: Inicializa o Gerenciador de componentes opcional.
ms.assetid: 9a7ddca6-a6c8-4d96-81bb-66158b83ab68
title: Função OcInitialize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcInitialize
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: aad102ac9881a801f693a429aab5dae07d09b5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748689"
---
# <a name="ocinitialize-function"></a><span data-ttu-id="5baca-103">Função OcInitialize</span><span class="sxs-lookup"><span data-stu-id="5baca-103">OcInitialize function</span></span>

<span data-ttu-id="5baca-104">Inicializa o Gerenciador de componentes opcional.</span><span class="sxs-lookup"><span data-stu-id="5baca-104">Initializes the optional component manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="5baca-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5baca-105">Syntax</span></span>


```C++
PVOID OcInitialize(
  _In_  POCM_CLIENT_CALLBACKS Callbacks,
  _In_  LPCTSTR               MasterOcInfName,
  _In_  UINT                  Flags,
  _Out_ PBOOL                 ShowError,
  _In_  PVOID                 Log
);
```



## <a name="parameters"></a><span data-ttu-id="5baca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5baca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5baca-107">*Retornos de chamada* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5baca-107">*Callbacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5baca-108">Um ponteiro para uma estrutura de [**\_ \_ retornos de chamada do cliente OCM**](ocm-client-callbacks.md) que especifica as funções de retorno de chamada a serem usadas pelo Gerenciador de OC para executar várias tarefas.</span><span class="sxs-lookup"><span data-stu-id="5baca-108">A pointer to an [**OCM\_CLIENT\_CALLBACKS**](ocm-client-callbacks.md) structure that specifies the callback functions to be used by the OC manager to perform various tasks.</span></span>

</dd> <dt>

<span data-ttu-id="5baca-109">*MasterOcInfName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5baca-109">*MasterOcInfName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5baca-110">O caminho do arquivo. inf do OC mestre.</span><span class="sxs-lookup"><span data-stu-id="5baca-110">The path of the master OC .inf file.</span></span>

</dd> <dt>

<span data-ttu-id="5baca-111">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="5baca-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5baca-112">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5baca-112">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="5baca-113"><span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**OCINIT \_ FORCENEWINF** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="5baca-113"><span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**OCINIT\_FORCENEWINF** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="5baca-114"><span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**OCINIT \_ KILLSUBCOMPS** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="5baca-114"><span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**OCINIT\_KILLSUBCOMPS** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="5baca-115"><span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**OCINIT \_ RUNQUIET** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="5baca-115"><span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**OCINIT\_RUNQUIET** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="5baca-116"><span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**OCINIT \_ LANGUAGEAWARE** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="5baca-116"><span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**OCINIT\_LANGUAGEAWARE** (0x00000008)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="5baca-117">*Erro* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="5baca-117">*ShowError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5baca-118">Se a função falhar, esse parâmetro indicará se uma mensagem de erro deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="5baca-118">If the function fails, this parameter indicates whether to display an error message.</span></span>

</dd> <dt>

<span data-ttu-id="5baca-119">*Log* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="5baca-119">*Log* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5baca-120">Um identificador para o log.</span><span class="sxs-lookup"><span data-stu-id="5baca-120">A handle to the log.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5baca-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5baca-121">Return value</span></span>

<span data-ttu-id="5baca-122">A função retorna o valor de contexto do Gerenciador do OC.</span><span class="sxs-lookup"><span data-stu-id="5baca-122">The function returns the OC manager context value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5baca-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="5baca-123">Remarks</span></span>

<span data-ttu-id="5baca-124">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="5baca-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5baca-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5baca-125">Requirements</span></span>



| <span data-ttu-id="5baca-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5baca-126">Requirement</span></span> | <span data-ttu-id="5baca-127">Valor</span><span class="sxs-lookup"><span data-stu-id="5baca-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5baca-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5baca-128">DLL</span></span><br/> | <dl> <span data-ttu-id="5baca-129"><dt>OcManage.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5baca-129"><dt>OcManage.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5baca-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="5baca-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5baca-131">**\_retornos de chamada do cliente OCM \_**</span><span class="sxs-lookup"><span data-stu-id="5baca-131">**OCM\_CLIENT\_CALLBACKS**</span></span>](ocm-client-callbacks.md)
</dt> <dt>

[<span data-ttu-id="5baca-132">**OcTerminate**</span><span class="sxs-lookup"><span data-stu-id="5baca-132">**OcTerminate**</span></span>](octerminate.md)
</dt> </dl>

 

 

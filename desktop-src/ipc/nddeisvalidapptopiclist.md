---
description: Determina se um aplicativo e uma cadeia de caracteres de tópico (&\# 0034; AppName \| topicname&\# 0034;) usa a sintaxe correta.
ms.assetid: bcf5442b-452e-4b42-95e9-f09bf885be40
title: Função NDdeIsValidAppTopicList (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidAppTopicList
- NDdeIsValidAppTopicListA
- NDdeIsValidAppTopicListW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: fb990830583f6684502438f132c1c98f5741a0ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105794454"
---
# <a name="nddeisvalidapptopiclist-function"></a><span data-ttu-id="43d6f-103">Função NDdeIsValidAppTopicList</span><span class="sxs-lookup"><span data-stu-id="43d6f-103">NDdeIsValidAppTopicList function</span></span>

<span data-ttu-id="43d6f-104">\[Não há mais suporte para DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="43d6f-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="43d6f-105">Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="43d6f-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="43d6f-106">Determina se um aplicativo e uma cadeia de caracteres de tópico ("*AppName* \| *topicname*") usam a sintaxe correta.</span><span class="sxs-lookup"><span data-stu-id="43d6f-106">Determines whether an application and topic string ("*AppName*\|*TopicName*") uses the proper syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="43d6f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43d6f-107">Syntax</span></span>


```C++
BOOL NDdeIsValidAppTopicList(
  _In_ LPTSTR targetTopic
);
```



## <a name="parameters"></a><span data-ttu-id="43d6f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43d6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43d6f-109">*targetTopic* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43d6f-109">*targetTopic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43d6f-110">Um ponteiro para a cadeia de caracteres do aplicativo e do tópico a ser validado.</span><span class="sxs-lookup"><span data-stu-id="43d6f-110">A pointer to the application and topic string to validate.</span></span> <span data-ttu-id="43d6f-111">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="43d6f-111">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43d6f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43d6f-112">Return value</span></span>

<span data-ttu-id="43d6f-113">Se o parâmetro *targetTopic* tiver uma sintaxe válida, o valor de retorno será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="43d6f-113">If the *targetTopic* parameter has valid syntax, the return value is nonzero.</span></span>

<span data-ttu-id="43d6f-114">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="43d6f-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="43d6f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="43d6f-115">Remarks</span></span>

<span data-ttu-id="43d6f-116">Essa função também é chamada por [**NDdeShareAdd**](nddeshareadd.md) quando cria o compartilhamento DDE.</span><span class="sxs-lookup"><span data-stu-id="43d6f-116">This function is also called by [**NDdeShareAdd**](nddeshareadd.md) when it creates the DDE share.</span></span>

## <a name="requirements"></a><span data-ttu-id="43d6f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43d6f-117">Requirements</span></span>



| <span data-ttu-id="43d6f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="43d6f-118">Requirement</span></span> | <span data-ttu-id="43d6f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="43d6f-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="43d6f-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43d6f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="43d6f-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="43d6f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="43d6f-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43d6f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="43d6f-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="43d6f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="43d6f-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="43d6f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="43d6f-125"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="43d6f-125"><dt>Nddeapi.h</dt></span></span> </dl>      |
| <span data-ttu-id="43d6f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43d6f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="43d6f-127"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43d6f-127"><dt>Nddeapi.lib</dt></span></span> </dl>    |
| <span data-ttu-id="43d6f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="43d6f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43d6f-129"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43d6f-129"><dt>Nddeapi.dll</dt></span></span> </dl>    |
| <span data-ttu-id="43d6f-130">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="43d6f-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="43d6f-131">**NDdeIsValidAppTopicListW** (Unicode) e **NDdeIsValidAppTopicListA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="43d6f-131">**NDdeIsValidAppTopicListW** (Unicode) and **NDdeIsValidAppTopicListA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43d6f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="43d6f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43d6f-133">Visão geral de troca dinâmica de dados de rede</span><span class="sxs-lookup"><span data-stu-id="43d6f-133">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="43d6f-134">Funções DDE de rede</span><span class="sxs-lookup"><span data-stu-id="43d6f-134">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="43d6f-135">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="43d6f-135">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 





---
description: A função BuildINIPath retorna um caminho totalmente qualificado para um arquivo INI que corresponde às informações inseridas.
ms.assetid: 214ce89c-8bb2-4e1a-872a-026743a3e3a6
title: Função BuildINIPath (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BuildINIPath
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3f715e740319515fe4772d1a9905a2f9b563f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756715"
---
# <a name="buildinipath-function"></a><span data-ttu-id="c30af-103">Função BuildINIPath</span><span class="sxs-lookup"><span data-stu-id="c30af-103">BuildINIPath function</span></span>

<span data-ttu-id="c30af-104">A função **BuildINIPath** retorna um caminho totalmente qualificado para um arquivo ini que corresponde às informações inseridas.</span><span class="sxs-lookup"><span data-stu-id="c30af-104">The **BuildINIPath** function returns a fully qualified path to an INI file that corresponds to information you enter.</span></span>

## <a name="syntax"></a><span data-ttu-id="c30af-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c30af-105">Syntax</span></span>


```C++
LPSTR BuildINIPath(
   char *FullPath,
   char *IniFileName
);
```



## <a name="parameters"></a><span data-ttu-id="c30af-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c30af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c30af-107">*FullPath*</span><span class="sxs-lookup"><span data-stu-id="c30af-107">*FullPath*</span></span> 
</dt> <dd>

<span data-ttu-id="c30af-108">Buffer que recebe o nome de arquivo INI totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="c30af-108">Buffer that receives the fully qualified INI file name.</span></span>

</dd> <dt>

<span data-ttu-id="c30af-109">*IniFileName*</span><span class="sxs-lookup"><span data-stu-id="c30af-109">*IniFileName*</span></span> 
</dt> <dd>

<span data-ttu-id="c30af-110">Nome do arquivo INI (o nome completo do arquivo menos a extensão de nome de arquivos).</span><span class="sxs-lookup"><span data-stu-id="c30af-110">Name of the INI file (the full file name minus the filename extension).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c30af-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c30af-111">Return value</span></span>

<span data-ttu-id="c30af-112">Se a função for bem-sucedida, o valor de retorno será um ponteiro para o nome de arquivo INI totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="c30af-112">If the function is successful, the return value is a pointer to the fully qualified INI file name.</span></span>

<span data-ttu-id="c30af-113">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c30af-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c30af-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c30af-114">Remarks</span></span>

<span data-ttu-id="c30af-115">O caminho que essa função retorna é um caminho totalmente qualificado para um arquivo INI que corresponde às informações inseridas.</span><span class="sxs-lookup"><span data-stu-id="c30af-115">The path that this function returns is a fully qualified path to an INI file that corresponds to information you enter.</span></span> <span data-ttu-id="c30af-116">Por exemplo, se você inserir XNS ou TCP, a função gerará um caminho para Xns.ini ou Tcp.ini, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c30af-116">For example, if you enter XNS or TCP, the function generates a path to Xns.ini or Tcp.ini, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="c30af-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c30af-117">Requirements</span></span>



| <span data-ttu-id="c30af-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c30af-118">Requirement</span></span> | <span data-ttu-id="c30af-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c30af-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c30af-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c30af-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c30af-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c30af-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c30af-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c30af-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c30af-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c30af-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c30af-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c30af-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c30af-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c30af-125"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="c30af-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c30af-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="c30af-127"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c30af-127"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="c30af-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c30af-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c30af-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c30af-129"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 





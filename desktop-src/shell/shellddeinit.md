---
description: Registra os serviços de troca dinâmica de dados de Shell (DDE) no processo atual, notificando o sistema de que o processo atual deseja hospedar objetos DDE.
ms.assetid: d7f65d6a-a697-475b-a739-c7950b7f4d5d
title: Função ShellDDEInit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellDDEInit
api_type:
- DllExport
api_location:
- Shdocvw.dll
ms.openlocfilehash: cb2f4639d97a99cd063f372e303fd48b7a1d6e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968123"
---
# <a name="shellddeinit-function"></a><span data-ttu-id="49685-103">Função ShellDDEInit</span><span class="sxs-lookup"><span data-stu-id="49685-103">ShellDDEInit function</span></span>

<span data-ttu-id="49685-104">Registra os serviços de troca dinâmica de dados de Shell (DDE) no processo atual, notificando o sistema de que o processo atual deseja hospedar objetos DDE.</span><span class="sxs-lookup"><span data-stu-id="49685-104">Registers the Shell Dynamic Data Exchange (DDE) services in the current process, notifying the system that the current process wishes to host DDE objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="49685-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49685-105">Syntax</span></span>


```C++
void ShellDDEInit(
  _In_ BOOL init
);
```



## <a name="parameters"></a><span data-ttu-id="49685-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49685-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49685-107">*init* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="49685-107">*init* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49685-108">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="49685-108">Type: **BOOL**</span></span>

<span data-ttu-id="49685-109">**True** para registrar o processo atual como host DDE; **False** para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="49685-109">**TRUE** to register the current process as DDE host; **FALSE** to unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49685-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="49685-110">Return value</span></span>

<span data-ttu-id="49685-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="49685-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49685-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="49685-112">Remarks</span></span>

<span data-ttu-id="49685-113">O processo que chama essa função atua como o Shell e é usado para exibir o conteúdo das pastas abertas com o verbo ' Open ' de [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="49685-113">The process that calls this function acts as the Shell and is used to view the content of folders opened with the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 'open' verb.</span></span>

<span data-ttu-id="49685-114">Essa função não tem um cabeçalho ou arquivo de biblioteca associado, portanto, ele deve ser chamado pelo valor ordinal.</span><span class="sxs-lookup"><span data-stu-id="49685-114">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="49685-115">Chame [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) com o nome da DLL (Shdocvw.dll) para obter um identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="49685-115">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Shdocvw.dll) to obtain a module handle.</span></span> <span data-ttu-id="49685-116">Em seguida, chame o [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com esse identificador de módulo e a função número ordinal 118 para obter o endereço da função.</span><span class="sxs-lookup"><span data-stu-id="49685-116">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the function ordinal number 118 to get the address of the function.</span></span>

## <a name="requirements"></a><span data-ttu-id="49685-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49685-117">Requirements</span></span>



| <span data-ttu-id="49685-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="49685-118">Requirement</span></span> | <span data-ttu-id="49685-119">Valor</span><span class="sxs-lookup"><span data-stu-id="49685-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49685-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49685-120">Minimum supported client</span></span><br/> | <span data-ttu-id="49685-121">Somente aplicativos de desktop do Windows XP, Windows 2000 Professional \[\]</span><span class="sxs-lookup"><span data-stu-id="49685-121">Windows XP, Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49685-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49685-122">Minimum supported server</span></span><br/> | <span data-ttu-id="49685-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="49685-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="49685-124">DLL</span><span class="sxs-lookup"><span data-stu-id="49685-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49685-125"><dt>Shdocvw.dll (versão 6,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="49685-125"><dt>Shdocvw.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 

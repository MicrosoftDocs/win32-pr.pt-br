---
description: Cria um moniker que representa um componente de hardware e seu manipulador de eventos associado. A reprodução automática usa essa função para permitir que os aplicativos usem eventos de reprodução automática.
title: Função CreateHardwareEventMoniker
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHardwareEventMoniker
api_type:
- DllExport
api_location:
- Shsvcs.dll
ms.assetid: ff0ad023-42ea-4c74-adae-af55527b6ac3
ms.openlocfilehash: 59100ab20cd997cc4ab35602698268ec6d76dea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967346"
---
# <a name="createhardwareeventmoniker-function"></a><span data-ttu-id="610ca-104">Função CreateHardwareEventMoniker</span><span class="sxs-lookup"><span data-stu-id="610ca-104">CreateHardwareEventMoniker function</span></span>

<span data-ttu-id="610ca-105">\[Essa função está disponível por meio do Windows XP com Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="610ca-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="610ca-106">Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="610ca-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="610ca-107">Cria um moniker que representa um componente de hardware e seu manipulador de eventos associado.</span><span class="sxs-lookup"><span data-stu-id="610ca-107">Creates a moniker representing a hardware component and its associated event handler.</span></span> <span data-ttu-id="610ca-108">A reprodução automática usa essa função para permitir que os aplicativos usem eventos de reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="610ca-108">AutoPlay uses this function to allow applications to use AutoPlay events.</span></span>

## <a name="syntax"></a><span data-ttu-id="610ca-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="610ca-109">Syntax</span></span>


```C++
HRESULT CreateHardwareEventMoniker(
  _In_  REFCLSID clsid,
  _In_  LPCTSTR  pszEventHandler,
  _Out_ IMoniker **ppmoniker
);
```



## <a name="parameters"></a><span data-ttu-id="610ca-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="610ca-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="610ca-111">*CLSID* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="610ca-111">*clsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="610ca-112">Tipo: **REFCLSID**</span><span class="sxs-lookup"><span data-stu-id="610ca-112">Type: **REFCLSID**</span></span>

<span data-ttu-id="610ca-113">A ID da classe à qual o moniker é associado.</span><span class="sxs-lookup"><span data-stu-id="610ca-113">The ID of the class to which the moniker binds.</span></span>

</dd> <dt>

<span data-ttu-id="610ca-114">*pszEventHandler* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="610ca-114">*pszEventHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="610ca-115">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="610ca-115">Type: **LPCTSTR**</span></span>

<span data-ttu-id="610ca-116">O nome do manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="610ca-116">The name of the event handler.</span></span>

</dd> <dt>

<span data-ttu-id="610ca-117">*ppmoniker* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="610ca-117">*ppmoniker* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="610ca-118">Tipo: **[ **IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***</span><span class="sxs-lookup"><span data-stu-id="610ca-118">Type: **[**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***</span></span>

<span data-ttu-id="610ca-119">O endereço de uma variável de ponteiro que recebe o ponteiro de interface [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) .</span><span class="sxs-lookup"><span data-stu-id="610ca-119">The address of a pointer variable that receives the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="610ca-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="610ca-120">Return value</span></span>

<span data-ttu-id="610ca-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="610ca-121">Type: **HRESULT**</span></span>

<span data-ttu-id="610ca-122">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="610ca-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="610ca-123">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="610ca-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="610ca-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="610ca-124">Remarks</span></span>

<span data-ttu-id="610ca-125">Use **CreateHardwareEventMoniker** ao registrar aplicativos em execução para que esses aplicativos tenham acesso aos eventos de reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="610ca-125">Use **CreateHardwareEventMoniker** when registering running applications so that those applications have access to AutoPlay events.</span></span> <span data-ttu-id="610ca-126">Para usar eventos de reprodução automática em aplicativos em execução, você deve primeiro criar um novo componente que implementa a interface [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .</span><span class="sxs-lookup"><span data-stu-id="610ca-126">To use AutoPlay events in running applications, you must first create a new component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span> <span data-ttu-id="610ca-127">Inicialize essa interface com o valor InitCmdLine da entrada do manipulador em particular sob a chave de **manipuladores** , porque a reprodução automática não chama o método [**Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) .</span><span class="sxs-lookup"><span data-stu-id="610ca-127">Initialize this interface with the InitCmdLine value from the particular handler's entry under the **Handlers** key, because AutoPlay does not call the [**Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) method.</span></span>

<span data-ttu-id="610ca-128">Você deve chamar **CreateHardwareEventMoniker** para obter um moniker que represente seu componente e seu manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="610ca-128">You should call **CreateHardwareEventMoniker** to get a moniker that represents your component and its event handler.</span></span> <span data-ttu-id="610ca-129">Em seguida, use o valor retornado no parâmetro *ppmoniker* para registrar seu componente na tabela de objetos em execução (corrompidos), conforme mostrado no exemplo.</span><span class="sxs-lookup"><span data-stu-id="610ca-129">Then, use the value returned in the *ppmoniker* parameter to register your component in the running object table (ROT) as shown in the example.</span></span>

<span data-ttu-id="610ca-130">Observe que **CreateHardwareEventMoniker** não está definido em um arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="610ca-130">Note that **CreateHardwareEventMoniker** is not defined in a header file.</span></span> <span data-ttu-id="610ca-131">Para usá-lo em seu código, você deve obter um identificador para o arquivo de Shsvcs.dll por meio de uma chamada para [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span><span class="sxs-lookup"><span data-stu-id="610ca-131">To use it in your code, you must obtain a handle to the Shsvcs.dll file through a call to [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span> <span data-ttu-id="610ca-132">Em seguida, você usa esse identificador em uma chamada para [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obter uma instância da função **CreateHardwareEventMoniker** .</span><span class="sxs-lookup"><span data-stu-id="610ca-132">You then use that handle in a call to [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain an instance of the **CreateHardwareEventMoniker** function.</span></span>

<span data-ttu-id="610ca-133">A chamada para [**IRunningObjectTable:: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) exige que você insira as seguintes informações de **AppID** no registro.</span><span class="sxs-lookup"><span data-stu-id="610ca-133">The call to [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requires that you enter the following **AppID** information in the registry.</span></span>

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="requirements"></a><span data-ttu-id="610ca-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="610ca-134">Requirements</span></span>



| <span data-ttu-id="610ca-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="610ca-135">Requirement</span></span> | <span data-ttu-id="610ca-136">Valor</span><span class="sxs-lookup"><span data-stu-id="610ca-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="610ca-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="610ca-137">Minimum supported client</span></span><br/> | <span data-ttu-id="610ca-138">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="610ca-138">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="610ca-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="610ca-139">Minimum supported server</span></span><br/> | <span data-ttu-id="610ca-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="610ca-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="610ca-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="610ca-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="610ca-142"><dt>Nenhum</dt></span><span class="sxs-lookup"><span data-stu-id="610ca-142"><dt>None</dt></span></span> </dl>       |
| <span data-ttu-id="610ca-143">DLL</span><span class="sxs-lookup"><span data-stu-id="610ca-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="610ca-144"><dt>Shsvcs.dll</dt></span><span class="sxs-lookup"><span data-stu-id="610ca-144"><dt>Shsvcs.dll</dt></span></span> </dl> |



 

 

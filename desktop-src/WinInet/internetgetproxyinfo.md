---
title: Função InternetGetProxyInfo
description: Recupera dados de proxy para acessar os recursos especificados.
ms.assetid: 5fc0f471-420c-4125-8323-cb1e1e72e43f
keywords:
- Função InternetGetProxyInfo WinINet
topic_type:
- apiref
api_name:
- InternetGetProxyInfo
api_location:
- JSProxy.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef441754fd5de09e3792d9269f05d96ecc08aa23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369631"
---
# <a name="internetgetproxyinfo-function"></a><span data-ttu-id="e586f-104">Função InternetGetProxyInfo</span><span class="sxs-lookup"><span data-stu-id="e586f-104">InternetGetProxyInfo function</span></span>

> [!NOTE]
> <span data-ttu-id="e586f-105">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="e586f-105">This function is deprecated.</span></span> <span data-ttu-id="e586f-106">Para obter suporte a AutoProxy, use o protocolo WinHTTP (HTTP Services) versão 5,1 em vez disso.</span><span class="sxs-lookup"><span data-stu-id="e586f-106">For autoproxy support, use HTTP Services (WinHTTP) version 5.1 instead.</span></span> <span data-ttu-id="e586f-107">Para obter mais informações, consulte [WinHTTP AutoProxy support](../winhttp/winhttp-autoproxy-support.md).</span><span class="sxs-lookup"><span data-stu-id="e586f-107">For more information, see [WinHTTP AutoProxy Support](../winhttp/winhttp-autoproxy-support.md).</span></span>

<span data-ttu-id="e586f-108">Recupera dados de proxy para acessar os recursos especificados.</span><span class="sxs-lookup"><span data-stu-id="e586f-108">Retrieves proxy data for accessing specified resources.</span></span> <span data-ttu-id="e586f-109">Essa função só pode ser chamada por meio da vinculação dinâmica a "JSProxy.dll".</span><span class="sxs-lookup"><span data-stu-id="e586f-109">This function can only be called by dynamically linking to "JSProxy.dll".</span></span>

## <a name="syntax"></a><span data-ttu-id="e586f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e586f-110">Syntax</span></span>

```cpp
BOOL InternetGetProxyInfo(
  _In_  LPCSTR  lpszUrl,
  _In_  DWORD   dwUrlLength,
  _In_  LPSTR   lpszUrlHostName,
  _In_  DWORD   dwUrlHostNameLength,
  _Out_ LPSTR   *lplpszProxyHostName,
  _Out_ LPDWORD lpdwProxyHostNameLength
);
```

## <a name="parameters"></a><span data-ttu-id="e586f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e586f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e586f-112">*lpszUrl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e586f-112">*lpszUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e586f-113">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a URL do recurso de HTTP de destino.</span><span class="sxs-lookup"><span data-stu-id="e586f-113">A pointer to a null-terminated string that specifies the URL of the target HTTP resource.</span></span>

</dd> <dt>

<span data-ttu-id="e586f-114">*dwUrlLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e586f-114">*dwUrlLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e586f-115">O tamanho, em bytes, da URL apontada por *lpszUrl*.</span><span class="sxs-lookup"><span data-stu-id="e586f-115">The size, in bytes, of the URL pointed to by *lpszUrl*.</span></span>

</dd> <dt>

<span data-ttu-id="e586f-116">*lpszUrlHostName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e586f-116">*lpszUrlHostName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e586f-117">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do host da URL de destino.</span><span class="sxs-lookup"><span data-stu-id="e586f-117">A pointer to a null-terminated string that specifies the host name of the target URL.</span></span>

</dd> <dt>

<span data-ttu-id="e586f-118">*dwUrlHostNameLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e586f-118">*dwUrlHostNameLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e586f-119">O tamanho, em bytes, do nome do host apontado por *lpszUrlHostName*.</span><span class="sxs-lookup"><span data-stu-id="e586f-119">The size, in bytes, of the host name pointed to by *lpszUrlHostName*.</span></span>

</dd> <dt>

<span data-ttu-id="e586f-120">*lplpszProxyHostName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e586f-120">*lplpszProxyHostName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e586f-121">Um ponteiro para o endereço de um buffer que recebe a URL do proxy a ser usada em uma solicitação HTTP para o recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="e586f-121">A pointer to the address of a buffer that receives the URL of the proxy to use in an HTTP request for the specified resource.</span></span> <span data-ttu-id="e586f-122">O aplicativo é responsável por liberar essa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e586f-122">The application is responsible for freeing this string.</span></span>

</dd> <dt>

<span data-ttu-id="e586f-123">*lpdwProxyHostNameLength* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e586f-123">*lpdwProxyHostNameLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e586f-124">Um ponteiro para uma variável que recebe o tamanho, em bytes, da cadeia de caracteres retornada no buffer *lplpszProxyHostName* .</span><span class="sxs-lookup"><span data-stu-id="e586f-124">A pointer to a variable that receives the size, in bytes, of the string returned in the *lplpszProxyHostName* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e586f-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e586f-125">Return value</span></span>

<span data-ttu-id="e586f-126">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="e586f-126">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="e586f-127">Para obter dados de erro estendidos, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="e586f-127">To get extended error data, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="e586f-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="e586f-128">Remarks</span></span>

<span data-ttu-id="e586f-129">Para chamar **InternetGetProxyInfo**, você deve vincular-se dinamicamente a ele usando o tipo de ponteiro de função definido **pfnInternetGetProxyInfo**.</span><span class="sxs-lookup"><span data-stu-id="e586f-129">To call **InternetGetProxyInfo**, you must dynamically link to it using the defined function-pointer type **pfnInternetGetProxyInfo**.</span></span> <span data-ttu-id="e586f-130">O trecho de código abaixo mostra como declarar uma instância desse tipo de ponteiro de função e, em seguida, inicializá-lo e chamá-lo.</span><span class="sxs-lookup"><span data-stu-id="e586f-130">The code snippet below shows how to declare an instance of this function-pointer type and then initialize and call it.</span></span>

```cpp
  HMODULE hModJS;                               // Handle for loading the DLL
  pfnInternetGetProxyInfo pIGPI;                // Function-pointer instance

  hModJS = LoadLibrary( TEXT("jsproxy.dll") );
  if (!hModJS)
  {
    _tprintf( TEXT("\nLoadLibrary failed to load jsproxy.dll with error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  pIGPI = (pfnInternetGetProxyInfo)
          GetProcAddress( hModJS, "InternetGetProxyInfo" );
  if (!pIGPI)         
  {
    _tprintf( TEXT("\nGetProcAddress failed to find InternetGetProxyInfo, error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  // The pIGPI function pointer can now be used to call InternetGetProxyInfo.
```

<span data-ttu-id="e586f-131">Como todos os outros aspectos da API do WinINet, essa função não pode ser chamada com segurança de em DllMain ou os construtores e destruidores de objetos globais.</span><span class="sxs-lookup"><span data-stu-id="e586f-131">Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.</span></span>

> [!Note]  
> <span data-ttu-id="e586f-132">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="e586f-132">WinINet does not support server implementations.</span></span> <span data-ttu-id="e586f-133">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="e586f-133">In addition, it should not be used from a service.</span></span> <span data-ttu-id="e586f-134">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="e586f-134">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

## <a name="requirements"></a><span data-ttu-id="e586f-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e586f-135">Requirements</span></span>

| <span data-ttu-id="e586f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="e586f-136">Requirement</span></span> | <span data-ttu-id="e586f-137">Valor</span><span class="sxs-lookup"><span data-stu-id="e586f-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e586f-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e586f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e586f-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e586f-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e586f-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e586f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e586f-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e586f-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e586f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e586f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e586f-143"><dt>JSProxy.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e586f-143"><dt>JSProxy.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="e586f-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="e586f-144">See also</span></span>

[<span data-ttu-id="e586f-145">**InternetInitializeAutoProxyDll**</span><span class="sxs-lookup"><span data-stu-id="e586f-145">**InternetInitializeAutoProxyDll**</span></span>](/windows/win32/api/winineti/nf-winineti-internetinitializeautoproxydll)

<span data-ttu-id="e586f-146">[**InternetDeInitializeAutoProxyDll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e586f-146">[**InternetDeInitializeAutoProxyDll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))</span></span>

[<span data-ttu-id="e586f-147">**DetectAutoProxyUrl**</span><span class="sxs-lookup"><span data-stu-id="e586f-147">**DetectAutoProxyUrl**</span></span>](/windows/win32/api/winineti/nf-winineti-detectautoproxyurl)

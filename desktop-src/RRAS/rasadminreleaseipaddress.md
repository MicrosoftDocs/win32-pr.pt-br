---
title: Função de retorno de chamada RasAdminReleaseIpAddress
description: A função RasAdminReleaseIpAddress é uma função definida pelo aplicativo que é exportada por uma DLL de administração de servidor RAS de terceiros.
ms.assetid: 86fd9173-f158-4de5-8166-483a652a52cc
keywords:
- Função de retorno de chamada RasAdminReleaseIpAddress RAS
topic_type:
- apiref
api_name:
- RasAdminReleaseIpAddress
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d58c162ebc6d340b9bd913407bc00aac87e208e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641728"
---
# <a name="rasadminreleaseipaddress-callback-function"></a><span data-ttu-id="3c32f-104">Função de retorno de chamada RasAdminReleaseIpAddress</span><span class="sxs-lookup"><span data-stu-id="3c32f-104">RasAdminReleaseIpAddress callback function</span></span>

<span data-ttu-id="3c32f-105">\[A função **RasAdminReleaseIpAddress** está disponível para uso no Windows NT 4,0 e não está disponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="3c32f-105">\[The **RasAdminReleaseIpAddress** function is available for use in Windows NT 4.0 and is unavailable in subsequent versions.</span></span> <span data-ttu-id="3c32f-106">Em vez disso, use [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]</span><span class="sxs-lookup"><span data-stu-id="3c32f-106">Instead, use [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]</span></span>

<span data-ttu-id="3c32f-107">A função **RasAdminReleaseIpAddress** é uma função definida pelo aplicativo que é exportada por uma DLL de administração de servidor RAS de terceiros.</span><span class="sxs-lookup"><span data-stu-id="3c32f-107">The **RasAdminReleaseIpAddress** function is an application-defined function that is exported by a third-party RAS server administration DLL.</span></span> <span data-ttu-id="3c32f-108">O RAS chama essa função para notificar a DLL de que o cliente remoto foi desconectado e que o endereço IP deve ser liberado.</span><span class="sxs-lookup"><span data-stu-id="3c32f-108">RAS calls this function to notify the DLL that the remote client was disconnected and that the IP address should be released.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c32f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c32f-109">Syntax</span></span>


```C++
void CALLBACK RasAdminReleaseIpAddress(
  _In_ WCHAR  *lpszUserName,
  _In_ WCHAR  *lpszPortName,
  _In_ IPADDR *pipAddress
);
```



## <a name="parameters"></a><span data-ttu-id="3c32f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c32f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c32f-111">*lpszUserName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3c32f-111">*lpszUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c32f-112">Especifica o ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome de um usuário remoto para o qual um endereço IP foi obtido anteriormente usando a função [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) .</span><span class="sxs-lookup"><span data-stu-id="3c32f-112">Specifies the pointer to a null-terminated Unicode string that specifies the name of a remote user for whom an IP address was previously obtained using the [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="3c32f-113">*lpszPortName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3c32f-113">*lpszPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c32f-114">Ponteiro para uma cadeia de caracteres Unicode terminada em nulo que especifica o nome da porta na qual o usuário especificado pelo *lpszUserName* está conectado.</span><span class="sxs-lookup"><span data-stu-id="3c32f-114">Pointer to a null-terminated Unicode string that specifies the name of the port on which the user specified by *lpszUserName* is connected.</span></span>

</dd> <dt>

<span data-ttu-id="3c32f-115">*pipAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3c32f-115">*pipAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c32f-116">Ponteiro para uma variável **IPADDR** que especifica o endereço IP retornado para esse usuário em uma chamada anterior para [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span><span class="sxs-lookup"><span data-stu-id="3c32f-116">Pointer to an **IPADDR** variable that specifies the IP address returned for this user in a previous call to [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c32f-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3c32f-117">Return value</span></span>

<span data-ttu-id="3c32f-118">Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="3c32f-118">There is no extended error information for this function; do no call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="3c32f-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c32f-119">Remarks</span></span>

<span data-ttu-id="3c32f-120">O servidor RAS chamará a função **RasAdminReleaseIpAddress** somente se o aplicativo retornar **true** no parâmetro *bNotifyRelease* durante a chamada anterior a [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) para o usuário especificado pelo parâmetro *lpszUserName* .</span><span class="sxs-lookup"><span data-stu-id="3c32f-120">The RAS server calls the **RasAdminReleaseIpAddress** function only if the application returned **TRUE** in the *bNotifyRelease* parameter during the earlier call to [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) for the user specified by the *lpszUserName* parameter.</span></span>

<span data-ttu-id="3c32f-121">O programa de instalação para uma DLL de administração de RAS de terceiros deve registrar a DLL com o RAS, fornecendo informações sob a seguinte chave no registro:</span><span class="sxs-lookup"><span data-stu-id="3c32f-121">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="3c32f-122">Para registrar a DLL, defina os valores a seguir nessa chave.</span><span class="sxs-lookup"><span data-stu-id="3c32f-122">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="3c32f-123">Nome do valor</span><span class="sxs-lookup"><span data-stu-id="3c32f-123">Value name</span></span>    | <span data-ttu-id="3c32f-124">Dados do valor</span><span class="sxs-lookup"><span data-stu-id="3c32f-124">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="3c32f-125">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="3c32f-125">*DisplayName*</span></span> | <span data-ttu-id="3c32f-126">Uma cadeia de caracteres **reg \_ sz** que contém o nome de exibição amigável da dll.</span><span class="sxs-lookup"><span data-stu-id="3c32f-126">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="3c32f-127">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="3c32f-127">*DLLPath*</span></span>     | <span data-ttu-id="3c32f-128">Uma cadeia de caracteres **reg \_ sz** que contém o caminho completo da dll.</span><span class="sxs-lookup"><span data-stu-id="3c32f-128">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="3c32f-129">Por exemplo, a entrada de registro para uma DLL de administração de RAS de uma empresa fictícia chamada proeletromagnéticon, Inc. pode ser:</span><span class="sxs-lookup"><span data-stu-id="3c32f-129">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc. might be:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="3c32f-130">*DisplayName*: **reg \_ sz** : dll de administração de Ras proeletromagnéticos *DLLPath*: **reg \_ sz** : C: \\ NT \\ System32 \\ntwkadm.dll</span><span class="sxs-lookup"><span data-stu-id="3c32f-130">*DisplayName*: **REG\_SZ** : ProElectron RAS Admin DLL *DLLPath*: **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll</span></span>

<span data-ttu-id="3c32f-131">O programa de instalação para uma DLL de administração de RAS também deve fornecer a funcionalidade de remoção/desinstalação.</span><span class="sxs-lookup"><span data-stu-id="3c32f-131">The setup program for a RAS administration DLL should also provide remove/uninstall functionality.</span></span> <span data-ttu-id="3c32f-132">Se um usuário remover a DLL, o programa de instalação deverá excluir as entradas do registro da DLL.</span><span class="sxs-lookup"><span data-stu-id="3c32f-132">If a user removes the DLL, the setup program should delete the DLL's registry entries.</span></span>

 

 
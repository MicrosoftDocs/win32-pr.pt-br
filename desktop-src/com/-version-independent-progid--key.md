---
title: Chave de ProgID independente de versão
description: Associa um ProgID a um CLSID. Essa chave é usada para determinar a versão mais recente de um aplicativo de objeto.
ms.assetid: fb43c8d0-d923-487f-afdf-14fc29a71e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a0bf379a06a6a05bb69a232ef91bb9fe81dc2f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454544"
---
# <a name="version-independent-progid-key"></a><span data-ttu-id="79952-104">Chave de ProgID independente de versão</span><span class="sxs-lookup"><span data-stu-id="79952-104">version-independent ProgID Key</span></span>

<span data-ttu-id="79952-105">Associa um ProgID a um CLSID.</span><span class="sxs-lookup"><span data-stu-id="79952-105">Associates a ProgID with a CLSID.</span></span> <span data-ttu-id="79952-106">Essa chave é usada para determinar a versão mais recente de um aplicativo de objeto.</span><span class="sxs-lookup"><span data-stu-id="79952-106">This key is used to determine the latest version of an object application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="79952-107">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="79952-107">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   <version-independent ProgID>
      CurVer = ProgID
```

## <a name="remarks"></a><span data-ttu-id="79952-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="79952-108">Remarks</span></span>

<span data-ttu-id="79952-109">A chave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde à chave de **\_ \_ raiz de classes hKey** , que foi retida para compatibilidade com versões anteriores do com.</span><span class="sxs-lookup"><span data-stu-id="79952-109">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

<span data-ttu-id="79952-110">O formato para <*ProgID> de versão* é <*programa*>. <*componente*>, separado por pontos, sem espaços e nenhum número de versão.</span><span class="sxs-lookup"><span data-stu-id="79952-110">The format for <*version-independent ProgID*> is <*program*>.<*component*>, separated by periods, no spaces, and no version number.</span></span> <span data-ttu-id="79952-111">O ProgID independente de versão, como o ProgID, pode ser registrado com um nome legível.</span><span class="sxs-lookup"><span data-stu-id="79952-111">The version-independent ProgID, like the ProgID, can be registered with a human-readable name.</span></span>

<span data-ttu-id="79952-112">*ProgID* é o ProgID da versão mais recente instalada da classe.</span><span class="sxs-lookup"><span data-stu-id="79952-112">*ProgID* is the ProgID of the latest installed version of the class.</span></span>

<span data-ttu-id="79952-113">Os aplicativos devem registrar um identificador programático independente de versão sob a chave *ProgID independente de versão* .</span><span class="sxs-lookup"><span data-stu-id="79952-113">Applications must register a version-independent programmatic identifier under the *version-independent ProgID* key.</span></span> <span data-ttu-id="79952-114">O ProgID independente de versão refere-se à classe do aplicativo e não muda de versão para versão, em vez disso, constante restante em todos os versionsâ € "por exemplo, documento do Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="79952-114">The version-independent ProgID refers to the application's class and does not change from version to version, instead remaining constant across all versionsâ€”for example, Microsoft Word Document.</span></span> <span data-ttu-id="79952-115">Ele é usado com linguagens de macro e refere-se à versão atualmente instalada da classe do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="79952-115">It is used with macro languages and refers to the currently installed version of the application's class.</span></span> <span data-ttu-id="79952-116">O ProgID independente de versão deve corresponder ao nome da versão mais recente do aplicativo de objeto.</span><span class="sxs-lookup"><span data-stu-id="79952-116">The version-independent ProgID must correspond to the name of the latest version of the object application.</span></span>

<span data-ttu-id="79952-117">Por exemplo, o ProgID independente de versão é usado quando um aplicativo de contêiner cria um gráfico ou uma tabela com um botão de barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="79952-117">For example, the version-independent ProgID is used when a container application creates a chart or table with a toolbar button.</span></span> <span data-ttu-id="79952-118">Nessa situação, o aplicativo pode usar o ProgID independente de versão para determinar a versão mais recente do aplicativo de objeto necessário.</span><span class="sxs-lookup"><span data-stu-id="79952-118">In this situation, the application can use the version-independent ProgID to determine the latest version of the needed object application.</span></span>

<span data-ttu-id="79952-119">O ProgID independente de versão é armazenado e mantido exclusivamente pelo código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="79952-119">The version-independent ProgID is stored and maintained solely by application code.</span></span> <span data-ttu-id="79952-120">Ao receber o ProgID independente de versão, a função [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) retorna o CLSID da versão atual.</span><span class="sxs-lookup"><span data-stu-id="79952-120">When given the version-independent ProgID, the [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) function returns the CLSID of the current version.</span></span>

<span data-ttu-id="79952-121">Você pode usar [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) e [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) para converter entre essas duas representações.</span><span class="sxs-lookup"><span data-stu-id="79952-121">You can use [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) and [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) to convert between these two representations.</span></span>

<span data-ttu-id="79952-122">Você pode usar [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) ou [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) para alterar o identificador para uma cadeia de caracteres que pode ser reproduzida.</span><span class="sxs-lookup"><span data-stu-id="79952-122">You can use [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) or [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) to change the identifier to a displayable string.</span></span>

<span data-ttu-id="79952-123">Se um manipulador personalizado não for usado, a entrada deverá ser definida como OLE32.DLL, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="79952-123">If a custom handler is not used, the entry should be set to OLE32.DLL, as shown in the following example:</span></span>

```
HKEY_CLASSES_ROOT\CLSID\{00000402-0000-0000-C000-000000000046}
   InprocHandler = ole32.dll
```

## <a name="related-topics"></a><span data-ttu-id="79952-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="79952-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79952-125">**CLSIDFromProgID**</span><span class="sxs-lookup"><span data-stu-id="79952-125">**CLSIDFromProgID**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid)
</dt> <dt>

[<span data-ttu-id="79952-126">**ProgIDFromCLSID**</span><span class="sxs-lookup"><span data-stu-id="79952-126">**ProgIDFromCLSID**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid)
</dt> <dt>

[<span data-ttu-id="79952-127"><ProgID> Chaves</span><span class="sxs-lookup"><span data-stu-id="79952-127"><ProgID> Key</span></span>](-progid--key.md)
</dt> </dl>

 

 





---
description: Retorna um objeto Recordlist que lista os produtos que usam um componente instalado especificado.
ms.assetid: c9756526-68d7-4d04-97e2-56a5eaf816be
title: Propriedade Installer. ClientsEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClientsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5a609ab0ba6edc5b0e3e9bbd26bc3539858ebdee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752253"
---
# <a name="installerclientsex-property"></a><span data-ttu-id="56fe0-103">Propriedade Installer. ClientsEx</span><span class="sxs-lookup"><span data-stu-id="56fe0-103">Installer.ClientsEx property</span></span>

<span data-ttu-id="56fe0-104">Essa propriedade retorna um objeto [**recordlist**](recordlist-object.md) que lista os produtos que usam um componente instalado especificado.</span><span class="sxs-lookup"><span data-stu-id="56fe0-104">This property returns a [**RecordList**](recordlist-object.md) object that lists products that use a specified installed component.</span></span> <span data-ttu-id="56fe0-105">Essa propriedade chama [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa).</span><span class="sxs-lookup"><span data-stu-id="56fe0-105">This property calls [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa).</span></span>

<span data-ttu-id="56fe0-106">**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="56fe0-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="56fe0-107">Essa propriedade está disponível a partir do Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="56fe0-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="56fe0-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="56fe0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="56fe0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56fe0-109">Syntax</span></span>


```JScript
propVal = Installer.ClientsEx
```



## <a name="property-value"></a><span data-ttu-id="56fe0-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="56fe0-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="56fe0-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56fe0-111">Requirements</span></span>



| <span data-ttu-id="56fe0-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="56fe0-112">Requirement</span></span> | <span data-ttu-id="56fe0-113">Valor</span><span class="sxs-lookup"><span data-stu-id="56fe0-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56fe0-114">Versão</span><span class="sxs-lookup"><span data-stu-id="56fe0-114">Version</span></span><br/> | <span data-ttu-id="56fe0-115">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="56fe0-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="56fe0-116">DLL</span><span class="sxs-lookup"><span data-stu-id="56fe0-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="56fe0-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56fe0-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="56fe0-118">IID</span><span class="sxs-lookup"><span data-stu-id="56fe0-118">IID</span></span><br/>     | <span data-ttu-id="56fe0-119">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="56fe0-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="56fe0-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="56fe0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56fe0-121">**MsiEnumClientsEx**</span><span class="sxs-lookup"><span data-stu-id="56fe0-121">**MsiEnumClientsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
</dt> </dl>

 

 





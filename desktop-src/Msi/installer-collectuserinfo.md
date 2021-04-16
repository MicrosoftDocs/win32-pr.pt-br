---
description: O método CollectUserInfo do objeto do instalador invoca uma sequência do assistente de interface do usuário que coleta e armazena informações do usuário e o código do produto.
ms.assetid: 2faacf38-1af1-4e8a-a3f6-87733104614e
title: Método Installer. CollectUserInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CollectUserInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d7286fdbc9fab6b3db6752284bf86db05f920bd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750235"
---
# <a name="installercollectuserinfo-method"></a><span data-ttu-id="cd19b-103">Método Installer. CollectUserInfo</span><span class="sxs-lookup"><span data-stu-id="cd19b-103">Installer.CollectUserInfo method</span></span>

<span data-ttu-id="cd19b-104">O método **CollectUserInfo** do objeto do [**instalador**](installer-object.md) invoca uma sequência do assistente de interface do usuário que coleta e armazena informações do usuário e o código do produto.</span><span class="sxs-lookup"><span data-stu-id="cd19b-104">The **CollectUserInfo** method of the [**Installer**](installer-object.md) object invokes a user interface wizard sequence which collects and stores both user information and the product code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd19b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd19b-105">Syntax</span></span>


```JScript
Installer.CollectUserInfo(
  Product
)
```



## <a name="parameters"></a><span data-ttu-id="cd19b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd19b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd19b-107">*Product*</span><span class="sxs-lookup"><span data-stu-id="cd19b-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="cd19b-108">Especifica o [**código do produto**](productcode.md) do produto.</span><span class="sxs-lookup"><span data-stu-id="cd19b-108">Specifies the [**product code**](productcode.md) of the product.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd19b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd19b-109">Return value</span></span>

<span data-ttu-id="cd19b-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cd19b-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd19b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd19b-111">Remarks</span></span>

<span data-ttu-id="cd19b-112">Um aplicativo deve chamar o método **CollectUserInfo** na primeira vez em que for executado.</span><span class="sxs-lookup"><span data-stu-id="cd19b-112">An application should call the **CollectUserInfo** method the first time it is run.</span></span> <span data-ttu-id="cd19b-113">O método **CollectUserInfo** abre o pacote de instalação do produto e invoca uma sequência de assistente de interface de usuário criada que coleta informações do usuário.</span><span class="sxs-lookup"><span data-stu-id="cd19b-113">The **CollectUserInfo** method opens the product's installation package and invokes an authored user interface wizard sequence which collects user information.</span></span> <span data-ttu-id="cd19b-114">Após a conclusão da sequência do assistente, as informações de usuário coletadas são registradas.</span><span class="sxs-lookup"><span data-stu-id="cd19b-114">Upon completion of the wizard sequence, the collected user information is registered.</span></span> <span data-ttu-id="cd19b-115">A propriedade [**UILevel**](installer-uilevel.md) deve ser definida como msiUILevelFull porque essa API requer uma interface de usuário criada.</span><span class="sxs-lookup"><span data-stu-id="cd19b-115">The [**UILevel**](installer-uilevel.md) property should be set to msiUILevelFull because this API requires an authored user interface.</span></span>

<span data-ttu-id="cd19b-116">O método **CollectUserInfo** invoca a [caixa de diálogo FirstRun](firstrun-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="cd19b-116">The **CollectUserInfo** method invokes the [FirstRun Dialog](firstrun-dialog.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd19b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd19b-117">Requirements</span></span>



| <span data-ttu-id="cd19b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd19b-118">Requirement</span></span> | <span data-ttu-id="cd19b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cd19b-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd19b-120">Versão</span><span class="sxs-lookup"><span data-stu-id="cd19b-120">Version</span></span><br/> | <span data-ttu-id="cd19b-121">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cd19b-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cd19b-122">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cd19b-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cd19b-123">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="cd19b-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="cd19b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cd19b-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="cd19b-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd19b-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="cd19b-126">IID</span><span class="sxs-lookup"><span data-stu-id="cd19b-126">IID</span></span><br/>     | <span data-ttu-id="cd19b-127">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="cd19b-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="cd19b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd19b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd19b-129">**MsiCollectUserInfo**</span><span class="sxs-lookup"><span data-stu-id="cd19b-129">**MsiCollectUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
</dt> </dl>

 

 





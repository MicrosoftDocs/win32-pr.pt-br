---
description: A propriedade TargetPath do objeto de sessão é uma propriedade de leitura/gravação que fornece o caminho completo para a pasta designada na unidade de destino da instalação.
ms.assetid: 563b874e-c669-4f5b-b3fa-eeb6b6e578f2
title: Propriedade Session. TargetPath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.TargetPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6c5917f845da0eec944e797d5f49f52d0ec26913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750216"
---
# <a name="sessiontargetpath-property"></a><span data-ttu-id="02871-103">Propriedade Session. TargetPath</span><span class="sxs-lookup"><span data-stu-id="02871-103">Session.TargetPath property</span></span>

<span data-ttu-id="02871-104">A propriedade **TargetPath** do objeto de [**sessão**](session-object.md) é uma propriedade de leitura/gravação que fornece o caminho completo para a pasta designada na unidade de destino da instalação.</span><span class="sxs-lookup"><span data-stu-id="02871-104">The **TargetPath** property of the [**Session**](session-object.md) object is a read-write property that provides the full path to the designated folder on the installation target drive.</span></span>

<span data-ttu-id="02871-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="02871-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="02871-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="02871-106">Syntax</span></span>


```JScript
propVal = Session.TargetPath
Session.TargetPath = propVal 
```



## <a name="property-value"></a><span data-ttu-id="02871-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="02871-107">Property value</span></span>

<span data-ttu-id="02871-108">Nome necessário diferenciar maiúsculas de minúsculas de uma propriedade de pasta, conforme especificado por uma chave primária da [tabela de diretórios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="02871-108">Required case-sensitive name of a folder property as specified by a primary key of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="02871-109">Um erro será gerado se a pasta não existir.</span><span class="sxs-lookup"><span data-stu-id="02871-109">An error is generated if the folder does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="02871-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="02871-110">Remarks</span></span>

<span data-ttu-id="02871-111">Não tente configurar o caminho de destino se os componentes que usam esses caminhos já estiverem instalados para o usuário atual ou para um usuário diferente.</span><span class="sxs-lookup"><span data-stu-id="02871-111">Do not attempt to configure the target path if the components using those paths are already installed for the current user or for a different user.</span></span> <span data-ttu-id="02871-112">Verifique a propriedade [**productstate**](productstate.md) para determinar se o produto que contém o componente está instalado.</span><span class="sxs-lookup"><span data-stu-id="02871-112">Check the [**ProductState**](productstate.md) property to determine if the product that contains the component is installed.</span></span>

<span data-ttu-id="02871-113">Se a propriedade falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="02871-113">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="02871-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02871-114">Requirements</span></span>



| <span data-ttu-id="02871-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="02871-115">Requirement</span></span> | <span data-ttu-id="02871-116">Valor</span><span class="sxs-lookup"><span data-stu-id="02871-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02871-117">Versão</span><span class="sxs-lookup"><span data-stu-id="02871-117">Version</span></span><br/> | <span data-ttu-id="02871-118">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="02871-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="02871-119">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="02871-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="02871-120">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="02871-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="02871-121">DLL</span><span class="sxs-lookup"><span data-stu-id="02871-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="02871-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02871-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="02871-123">IID</span><span class="sxs-lookup"><span data-stu-id="02871-123">IID</span></span><br/>     | <span data-ttu-id="02871-124">IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="02871-124">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 





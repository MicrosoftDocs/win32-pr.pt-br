---
description: O método SetInstallLevel do objeto Session define o nível de instalação para a instalação atual com um valor especificado e recalcula os Estados Select e installed para todos os recursos na tabela de recursos.
ms.assetid: d47f8025-d484-42c7-9808-5ee590a4d200
title: Método Session. SetInstallLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SetInstallLevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: abb5ff5f7a528ff654787e9b2ee3d935abee57d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751628"
---
# <a name="sessionsetinstalllevel-method"></a><span data-ttu-id="9d251-103">Método Session. SetInstallLevel</span><span class="sxs-lookup"><span data-stu-id="9d251-103">Session.SetInstallLevel method</span></span>

<span data-ttu-id="9d251-104">O método **SetInstallLevel** do objeto [**Session**](session-object.md) define o nível de instalação para a instalação atual com um valor especificado e recalcula os Estados Select e installed para todos os recursos na tabela de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d251-104">The **SetInstallLevel** method of the [**Session**](session-object.md) object sets the install level for the current installation to a specified value and recalculates the Select and Installed states for all features in the Feature table.</span></span> <span data-ttu-id="9d251-105">Ele também define o estado de ação de cada componente na [tabela de componentes](component-table.md) com base no novo nível.</span><span class="sxs-lookup"><span data-stu-id="9d251-105">It also sets the Action state of each component in the [Component table](component-table.md) based on the new level.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d251-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d251-106">Syntax</span></span>


```JScript
Session.SetInstallLevel(
  installLevel
)
```



## <a name="parameters"></a><span data-ttu-id="9d251-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d251-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d251-108">*installLevel*</span><span class="sxs-lookup"><span data-stu-id="9d251-108">*installLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="9d251-109">Novo nível de instalação solicitado necessário.</span><span class="sxs-lookup"><span data-stu-id="9d251-109">Required requested new install level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d251-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9d251-110">Return value</span></span>

<span data-ttu-id="9d251-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9d251-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d251-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d251-112">Remarks</span></span>

<span data-ttu-id="9d251-113">A [ação CostInitialize](costinitialize-action.md) deve ser executada antes de chamar **SetInstallLevel**.</span><span class="sxs-lookup"><span data-stu-id="9d251-113">The [CostInitialize action](costinitialize-action.md) must be executed prior to calling **SetInstallLevel**.</span></span>

<span data-ttu-id="9d251-114">Se 0 for passado para o parâmetro *installLevel* , o nível de instalação atual não será alterado, mas todos os recursos ainda serão atualizados com base no nível de instalação atual.</span><span class="sxs-lookup"><span data-stu-id="9d251-114">If 0 is passed for the *installLevel* parameter, the current install level is not changed, but all features are still updated based on the current install level.</span></span> <span data-ttu-id="9d251-115">Por exemplo, essa funcionalidade pode ser usada pelo módulo manipulador para redefinir todas as seleções de volta para seus Estados padrão iniciais em qualquer ponto do processo de seleção de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="9d251-115">For example, this functionality could be used by the Handler module to reset all selections back to their initial default states at any point in the UI selection process.</span></span>

<span data-ttu-id="9d251-116">Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="9d251-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d251-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d251-117">Requirements</span></span>



| <span data-ttu-id="9d251-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d251-118">Requirement</span></span> | <span data-ttu-id="9d251-119">Valor</span><span class="sxs-lookup"><span data-stu-id="9d251-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d251-120">Versão</span><span class="sxs-lookup"><span data-stu-id="9d251-120">Version</span></span><br/> | <span data-ttu-id="9d251-121">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9d251-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9d251-122">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9d251-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9d251-123">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="9d251-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="9d251-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9d251-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="9d251-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d251-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="9d251-126">IID</span><span class="sxs-lookup"><span data-stu-id="9d251-126">IID</span></span><br/>     | <span data-ttu-id="9d251-127">IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9d251-127">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 





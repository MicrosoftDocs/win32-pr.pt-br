---
description: O método Commit do objeto Database finaliza a forma persistente do banco de dados.
ms.assetid: 39253ccd-08f1-4a6f-87cb-3678ae5221a4
title: Método Database. Commit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Commit
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d62c998a70e0a4a036695be10b2bf1d983044241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752048"
---
# <a name="databasecommit-method"></a><span data-ttu-id="e6079-103">Método Database. Commit</span><span class="sxs-lookup"><span data-stu-id="e6079-103">Database.Commit method</span></span>

<span data-ttu-id="e6079-104">O método **Commit** do objeto [**Database**](database-object.md) finaliza a forma persistente do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e6079-104">The **Commit** method of the [**Database**](database-object.md) object finalizes the persistent form of the database.</span></span> <span data-ttu-id="e6079-105">Todos os dados persistentes são gravados no banco de dado gravável e nenhuma coluna ou linha temporária é gravada.</span><span class="sxs-lookup"><span data-stu-id="e6079-105">All persistent data is written to the writeable database, and no temporary columns or rows are written.</span></span> <span data-ttu-id="e6079-106">Esse método não tem efeito em um banco de dados aberto como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e6079-106">This method has no effect on a database opened as read-only.</span></span> <span data-ttu-id="e6079-107">Esse método pode ser chamado várias vezes para salvar o estado atual das tabelas carregadas na memória.</span><span class="sxs-lookup"><span data-stu-id="e6079-107">This method can be called multiple times to save the current state of tables loaded into memory.</span></span> <span data-ttu-id="e6079-108">Quando o banco de dados é finalmente fechado, as alterações feitas subsequentemente na última **confirmação** são revertidas.</span><span class="sxs-lookup"><span data-stu-id="e6079-108">When the database is finally closed, any changes made subsequent to the last **Commit** are rolled back.</span></span> <span data-ttu-id="e6079-109">Esse método é normalmente chamado antes do desligamento quando todas as alterações de banco de dados tiverem sido finalizadas.</span><span class="sxs-lookup"><span data-stu-id="e6079-109">This method is normally called prior to shutdown when all database changes have been finalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6079-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6079-110">Syntax</span></span>


```JScript
Database.Commit()
```



## <a name="parameters"></a><span data-ttu-id="e6079-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6079-111">Parameters</span></span>

<span data-ttu-id="e6079-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e6079-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6079-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6079-113">Return value</span></span>

<span data-ttu-id="e6079-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e6079-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6079-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6079-115">Remarks</span></span>

<span data-ttu-id="e6079-116">Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="e6079-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6079-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6079-117">Requirements</span></span>



| <span data-ttu-id="e6079-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6079-118">Requirement</span></span> | <span data-ttu-id="e6079-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e6079-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6079-120">Versão</span><span class="sxs-lookup"><span data-stu-id="e6079-120">Version</span></span><br/> | <span data-ttu-id="e6079-121">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e6079-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e6079-122">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e6079-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e6079-123">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e6079-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e6079-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e6079-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="e6079-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6079-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e6079-126">IID</span><span class="sxs-lookup"><span data-stu-id="e6079-126">IID</span></span><br/>     | <span data-ttu-id="e6079-127">IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e6079-127">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 





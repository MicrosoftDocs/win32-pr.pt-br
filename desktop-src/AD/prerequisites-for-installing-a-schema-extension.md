---
title: Pré-requisitos para instalar uma extensão de esquema
description: Para modificar o esquema, verifique se você tem os direitos a seguir e se está ciente das informações a seguir que você deve ter direitos suficientes para modificar o esquema.
ms.assetid: f7795eac-2b95-4b6c-a2f5-8728316059ab
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 275f468df54b9ced3dcca0648e4cc3602ab71422
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104293805"
---
# <a name="prerequisites-for-installing-a-schema-extension"></a><span data-ttu-id="29971-103">Pré-requisitos para instalar uma extensão de esquema</span><span class="sxs-lookup"><span data-stu-id="29971-103">Prerequisites for Installing a Schema Extension</span></span>

<span data-ttu-id="29971-104">Para modificar o esquema, verifique se você tem os direitos a seguir e se está ciente das seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="29971-104">To modify the schema, ensure you have the following rights and are aware of the following information:</span></span>

-   <span data-ttu-id="29971-105">Você deve ter direitos suficientes para modificar o esquema.</span><span class="sxs-lookup"><span data-stu-id="29971-105">You must have sufficient rights to modify the schema.</span></span> <span data-ttu-id="29971-106">O esquema contém todas as definições de dados para Active Directory Domain Services para toda a empresa.</span><span class="sxs-lookup"><span data-stu-id="29971-106">The schema contains all of the data definitions for Active Directory Domain Services for the entire enterprise.</span></span> <span data-ttu-id="29971-107">Para atualizar o esquema, um usuário deve ser membro do grupo Administradores de esquema ou ter recebido os direitos para atualizar o esquema.</span><span class="sxs-lookup"><span data-stu-id="29971-107">To update the schema, a user must be a member of the Schema Administrators group, or have been delegated the rights to update the schema.</span></span>
-   <span data-ttu-id="29971-108">Você só pode fazer alterações de esquema no mestre de esquema.</span><span class="sxs-lookup"><span data-stu-id="29971-108">You can only make schema changes at the schema master.</span></span> <span data-ttu-id="29971-109">Para obter mais informações, consulte [detectando o mestre de esquema](detecting-the-schema-master.md).</span><span class="sxs-lookup"><span data-stu-id="29971-109">For more information, see [Detecting the Schema Master](detecting-the-schema-master.md).</span></span>
-   <span data-ttu-id="29971-110">O mestre de esquema deve ser gravável; ou seja, o bloqueio de segurança no registro deve ser removido.</span><span class="sxs-lookup"><span data-stu-id="29971-110">The schema master must be writable; that is, the safety interlock in the registry must be removed.</span></span> <span data-ttu-id="29971-111">Para obter mais informações, consulte [habilitando alterações de esquema no mestre de esquema](enabling-schema-changes-at-the-schema-master.md).</span><span class="sxs-lookup"><span data-stu-id="29971-111">For more information, see [Enabling Schema Changes at the Schema Master](enabling-schema-changes-at-the-schema-master.md).</span></span>
-   <span data-ttu-id="29971-112">Para obter mais informações sobre como verificar se o mestre de esquema pode ser modificado e como alterar suas configurações, consulte "XADM: não é possível atualizar o esquema no proprietário do esquema" na base de dados de conhecimento de ajuda e suporte em [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .</span><span class="sxs-lookup"><span data-stu-id="29971-112">For more information about how to check whether the schema master can be modified, and how to change its settings, see "XADM: Unable to Update the Schema on the Schema Owner" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .</span></span>

 

 





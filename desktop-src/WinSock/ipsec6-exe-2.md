---
description: A configuração de políticas IPSec e associações de segurança para IPv6 é feita com Ipsec6.exe.
ms.assetid: 9a0c8e48-bc57-461d-9ade-54b75f7aa56d
title: Ipsec6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b373e8ab0dc54c3c8ee2fae8bc05722a9ac6aa64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764264"
---
# <a name="ipsec6exe"></a><span data-ttu-id="d5924-103">Ipsec6.exe</span><span class="sxs-lookup"><span data-stu-id="d5924-103">Ipsec6.exe</span></span>

<span data-ttu-id="d5924-104">A configuração de políticas IPSec e associações de segurança para IPv6 é feita com Ipsec6.exe.</span><span class="sxs-lookup"><span data-stu-id="d5924-104">Configuration of IPSec policies and security associations for IPv6 is done with Ipsec6.exe.</span></span> <span data-ttu-id="d5924-105">A seguir estão Ipsec6.exe subcomandos:</span><span class="sxs-lookup"><span data-stu-id="d5924-105">The following are Ipsec6.exe subcommands:</span></span>

<dl> <dt>

<span data-ttu-id="d5924-106"><span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>**Ipsec6 SP \[** _Interface_ do *_\]_*</span><span class="sxs-lookup"><span data-stu-id="d5924-106"><span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>**ipsec6 sp \[**_Interface_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="d5924-107">Exibe as políticas de segurança ativas.</span><span class="sxs-lookup"><span data-stu-id="d5924-107">Displays active security policies.</span></span> <span data-ttu-id="d5924-108">Como alternativa, exibe as políticas de segurança ativas para uma interface específica.</span><span class="sxs-lookup"><span data-stu-id="d5924-108">Alternately, displays active security policies for a specific interface.</span></span>

</dd> <dt>

<span data-ttu-id="d5924-109"><span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**Ipsec6 SA**</span><span class="sxs-lookup"><span data-stu-id="d5924-109"><span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**ipsec6 sa**</span></span>
</dt> <dd>

<span data-ttu-id="d5924-110">Exibe associações de segurança ativas.</span><span class="sxs-lookup"><span data-stu-id="d5924-110">Displays active security associations.</span></span>

</dd> <dt>

<span data-ttu-id="d5924-111"><span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**Ipsec6 c \[** _Nome do arquivo (sem extensão)_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="d5924-111"><span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 c \[**_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="d5924-112">Cria arquivos usados para configurar as associações de segurança e política de segurança.</span><span class="sxs-lookup"><span data-stu-id="d5924-112">Creates files used to configure security policy and security associations.</span></span> <span data-ttu-id="d5924-113">Cria *filename*. SPD para políticas de segurança e *filename*. sad para associações de segurança.</span><span class="sxs-lookup"><span data-stu-id="d5924-113">Creates *FileName*.spd for security policies and *FileName*.sad for security associations.</span></span> <span data-ttu-id="d5924-114">Use os arquivos criados como modelos para configurar políticas de segurança ou associações de segurança.</span><span class="sxs-lookup"><span data-stu-id="d5924-114">Use the created files as templates to configure security policies or security associations.</span></span> <span data-ttu-id="d5924-115">Os arquivos podem ser modificados com um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="d5924-115">The files can be modified with a text editor.</span></span> <span data-ttu-id="d5924-116">Para invocar a configuração contida nos arquivos SPD e SAD, use o comando **Ipsec6 a** .</span><span class="sxs-lookup"><span data-stu-id="d5924-116">To invoke the configuration contained in the SPD and SAD files, use the **ipsec6 a** command.</span></span>

</dd> <dt>

<span data-ttu-id="d5924-117"><span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**Ipsec6 a \[** _Nome do arquivo (sem extensão)_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="d5924-117"><span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 a \[**_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="d5924-118">Adiciona políticas de segurança em *filename*. SPD e associações de segurança em *filename*. sad à lista de políticas de segurança ativas e associações de segurança.</span><span class="sxs-lookup"><span data-stu-id="d5924-118">Adds security policies in *FileName*.spd and security associations in *FileName*.sad to the list of active security policies and security associations.</span></span>

</dd> <dt>

<span data-ttu-id="d5924-119"><span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**Ipsec6 i \[**  *_\] \[_* _Nome de arquivo da política (sem extensão)_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="d5924-119"><span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 i \[**_Policy_*_\] \[_*_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="d5924-120">Adiciona políticas de segurança em *filename*. SPD e associações de segurança em *filename*. sad à lista de políticas de segurança ativas e associações de segurança, conforme referenciado pelo número da política.</span><span class="sxs-lookup"><span data-stu-id="d5924-120">Adds security policies in *FileName*.spd and security associations in *FileName*.sad to the list of active security policies and security associations as referenced by policy number.</span></span>

</dd> <dt>

<span data-ttu-id="d5924-121"><span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**Ipsec6 d \[ Type = SP SA \] \[** _IndexNumber_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="d5924-121"><span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**ipsec6 d \[type = sp sa\] \[**_IndexNumber_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="d5924-122">Exclui políticas de segurança ou associações de segurança da lista de políticas de segurança ativas e associações de segurança, conforme referenciado pelo seu número de índice (exibido com **Ipsec6 SP** ou **Ipsec6 SA**).</span><span class="sxs-lookup"><span data-stu-id="d5924-122">Deletes security policies or security associations from the list of active security policies and security associations, as referenced by their index number (displayed with **ipsec6 sp** or **ipsec6 sa**).</span></span>

</dd> </dl>

 

 




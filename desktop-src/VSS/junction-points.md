---
description: No Windows Vista e no Windows Server 2008, os locais padrão para dados do usuário e dados do sistema foram alterados.
ms.assetid: 78679851-91f5-447f-8580-12cbf0323fb8
title: Pontos de junção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f1823c67e2c6b95ae366b7604054b47305062e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797490"
---
# <a name="junction-points"></a><span data-ttu-id="08734-103">Pontos de junção</span><span class="sxs-lookup"><span data-stu-id="08734-103">Junction Points</span></span>

<span data-ttu-id="08734-104">No Windows Vista e no Windows Server 2008, os locais padrão para dados do usuário e dados do sistema foram alterados.</span><span class="sxs-lookup"><span data-stu-id="08734-104">In Windows Vista and Windows Server 2008, the default locations for user data and system data have changed.</span></span> <span data-ttu-id="08734-105">Por exemplo, os dados do usuário armazenados anteriormente no diretório de documentos e configurações do% SystemDrive% \\ agora são armazenados no diretório% systemdrive% \\ usuários.</span><span class="sxs-lookup"><span data-stu-id="08734-105">For example, user data that was previously stored in the %SystemDrive%\\Documents and Settings directory is now stored in the %SystemDrive%\\Users directory.</span></span> <span data-ttu-id="08734-106">Para compatibilidade com versões anteriores, os locais antigos têm pontos de junção que apontam para os novos locais.</span><span class="sxs-lookup"><span data-stu-id="08734-106">For backward compatibility, the old locations have junction points that point to the new locations.</span></span> <span data-ttu-id="08734-107">Por exemplo, C: \\ Documents and Settings agora é um ponto de junção que aponta para C: \\ users.</span><span class="sxs-lookup"><span data-stu-id="08734-107">For example, C:\\Documents and Settings is now a junction point that points to C:\\Users.</span></span> <span data-ttu-id="08734-108">Os aplicativos de backup devem ser capazes de fazer backup e restaurar pontos de junção.</span><span class="sxs-lookup"><span data-stu-id="08734-108">Backup applications must be capable of backing up and restoring junction points.</span></span>

<span data-ttu-id="08734-109">Esses pontos de junção podem ser identificados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="08734-109">These junction points can be identified as follows:</span></span>

-   <span data-ttu-id="08734-110">Eles têm o \_ ponto de nova análise de atributo de arquivo, o atributo de \_ \_ arquivo \_ \_ oculto e os atributos de arquivo do sistema de atributo de arquivo \_ \_ definidos.</span><span class="sxs-lookup"><span data-stu-id="08734-110">They have the FILE\_ATTRIBUTE\_REPARSE\_POINT, FILE\_ATTRIBUTE\_HIDDEN, and FILE\_ATTRIBUTE\_SYSTEM file attributes set.</span></span>
-   <span data-ttu-id="08734-111">Eles também têm suas ACLs (listas de controle de acesso) definidas para negar acesso de leitura a todos.</span><span class="sxs-lookup"><span data-stu-id="08734-111">They also have their access control lists (ACLs) set to deny read access to everyone.</span></span>

<span data-ttu-id="08734-112">Os aplicativos que chamam um caminho específico podem atravessar esses pontos de junção se tiverem as permissões necessárias.</span><span class="sxs-lookup"><span data-stu-id="08734-112">Applications that call out a specific path can traverse these junction points if they have the required permissions.</span></span> <span data-ttu-id="08734-113">No entanto, as tentativas de enumerar o conteúdo dos pontos de junção resultarão em falhas.</span><span class="sxs-lookup"><span data-stu-id="08734-113">However, attempts to enumerate the contents of the junction points will result in failures.</span></span> <span data-ttu-id="08734-114">É importante que os aplicativos de backup não percorram esses pontos de junção ou tentem fazer backup de dados sob eles, por dois motivos:</span><span class="sxs-lookup"><span data-stu-id="08734-114">It is important that backup applications do not traverse these junction points, or attempt to backup data under them, for two reasons:</span></span>

-   <span data-ttu-id="08734-115">Isso pode fazer com que o aplicativo de backup faça backup dos mesmos dados mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="08734-115">Doing so can cause the backup application to back up the same data more than once.</span></span>
-   <span data-ttu-id="08734-116">Ele também pode levar a ciclos (referências circulares).</span><span class="sxs-lookup"><span data-stu-id="08734-116">It can also lead to cycles (circular references).</span></span>

## <a name="per-user-junctions-and-system-junctions"></a><span data-ttu-id="08734-117">Junções de Per-User e junções de sistema</span><span class="sxs-lookup"><span data-stu-id="08734-117">Per-User Junctions and System Junctions</span></span>

<span data-ttu-id="08734-118">Os pontos de junção usados para fornecer a virtualização de arquivo e registro no Windows Vista e no Windows Server 2008 podem ser divididos em duas classes: junções por usuário e junções de sistema.</span><span class="sxs-lookup"><span data-stu-id="08734-118">The junction points that are used to provide file and registry virtualization in Windows Vista and Windows Server 2008 can be divided into two classes: per-user junctions and system junctions.</span></span>

<span data-ttu-id="08734-119">As junções por usuário são criadas dentro de cada perfil de usuário individual para fornecer compatibilidade com versões anteriores para aplicativos de usuário.</span><span class="sxs-lookup"><span data-stu-id="08734-119">Per-user junctions are created inside each individual user's profile to provide backward compatibility for user applications.</span></span> <span data-ttu-id="08734-120">O ponto de junção em C: \\ Users \\ *username* \\ My Documents que aponta para C: \\ Users \\ *username* \\ Documents é um exemplo de uma junção por usuário.</span><span class="sxs-lookup"><span data-stu-id="08734-120">The junction point at C:\\Users\\*username*\\My Documents that points to C:\\Users\\*username*\\Documents is an example of a per-user junction.</span></span> <span data-ttu-id="08734-121">As junções por usuário são criadas pelo serviço de perfil quando o perfil do usuário é criado.</span><span class="sxs-lookup"><span data-stu-id="08734-121">Per-user junctions are created by the Profile service when the user's profile is created.</span></span>

<span data-ttu-id="08734-122">As outras junções são junções de sistema que não residem no diretório Users \\ *username* .</span><span class="sxs-lookup"><span data-stu-id="08734-122">The other junctions are system junctions that do not reside under the Users\\*username* directory.</span></span> <span data-ttu-id="08734-123">Exemplos de junções de sistema incluem:</span><span class="sxs-lookup"><span data-stu-id="08734-123">Examples of system junctions include:</span></span>

-   <span data-ttu-id="08734-124">Documentos e configurações</span><span class="sxs-lookup"><span data-stu-id="08734-124">Documents and Settings</span></span>
-   <span data-ttu-id="08734-125">Junções dentro de todos os usuários, públicos e perfis de usuário padrão</span><span class="sxs-lookup"><span data-stu-id="08734-125">Junctions within the All Users, Public, and Default User profiles</span></span>

<span data-ttu-id="08734-126">As junções do sistema são criadas por userenv.dll quando ele é invocado pelo Windows Welcome (também chamado de máquina de experiência mOOBE).</span><span class="sxs-lookup"><span data-stu-id="08734-126">System junctions are created by userenv.dll when it is invoked by Windows Welcome (also called the machine out-of-box-experience, or mOOBE).</span></span>

> [!Note]  
> <span data-ttu-id="08734-127">Se o usuário alterar o idioma do sistema para um idioma diferente do inglês, os pontos de junção por usuário e sistema serão criados com nomes localizados.</span><span class="sxs-lookup"><span data-stu-id="08734-127">If the user changes the system language to a language other than English, the per-user and system junction points will be created with localized names.</span></span>

 

 

 




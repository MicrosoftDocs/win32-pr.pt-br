---
title: ADSI e controle de conta de usuário
description: O Windows e o Windows Server têm controle de conta de usuário, que tem ramificações para aplicativos que usam ADSI (Active Directory Service Interfaces).
ms.assetid: 0b286252-8c24-4a18-9dc6-063ca158a8ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36fc88169a8710228a3bf70283aaccd4b4ac42e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008360"
---
# <a name="adsi-and-user-account-control"></a><span data-ttu-id="5d0ee-103">ADSI e controle de conta de usuário</span><span class="sxs-lookup"><span data-stu-id="5d0ee-103">ADSI and User Account Control</span></span>

<span data-ttu-id="5d0ee-104">O Windows e o Windows Server têm [controle de conta de usuário](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)), que tem ramificações para aplicativos que usam ADSI ( [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) ).</span><span class="sxs-lookup"><span data-stu-id="5d0ee-104">Windows and Windows Server have [User Account Control](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)), which has ramifications for applications that use [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span></span> <span data-ttu-id="5d0ee-105">Especificamente, essas interfaces foram projetadas para serem executadas por uma conta de usuário com privilégios de administrador no computador local.</span><span class="sxs-lookup"><span data-stu-id="5d0ee-105">Specifically, these interfaces were designed to be run by a user account with administrator privileges on the local computer.</span></span>

<span data-ttu-id="5d0ee-106">**Problema**</span><span class="sxs-lookup"><span data-stu-id="5d0ee-106">**Problem**</span></span>

<span data-ttu-id="5d0ee-107">Toda vez que um aplicativo se conecta ao diretório e tenta criar um objeto ADSI, o [esquema de Active Directory](/windows/desktop/ADSchema/active-directory-schema) é verificado quanto a alterações.</span><span class="sxs-lookup"><span data-stu-id="5d0ee-107">Every time an application connects to the directory and attempts to create an ADSI object, the [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) is checked for changes.</span></span> <span data-ttu-id="5d0ee-108">Se ele foi alterado desde a última conexão, o esquema é baixado e armazenado em um cache no computador local.</span><span class="sxs-lookup"><span data-stu-id="5d0ee-108">If it has changed since the last connection, the schema is downloaded and stored in a cache on the local computer.</span></span> <span data-ttu-id="5d0ee-109">Em versões do Windows anteriores ao Windows Vista, o local padrão desse cache era</span><span class="sxs-lookup"><span data-stu-id="5d0ee-109">In versions of Windows prior to Windows Vista, the default location for this cache was</span></span>

`%systemroot%\SchCache\`

<span data-ttu-id="5d0ee-110">No entanto, os aplicativos executados por contas padrão (ou seja, não administrador) não terão acesso a esse diretório e, consequentemente, os aplicativos que usam interfaces ADSI executadas nesse modo baixarão o esquema em cada conexão, o que afetará a taxa de transferência e o desempenho.</span><span class="sxs-lookup"><span data-stu-id="5d0ee-110">However, applications run by standard (that is, non-administrator) accounts will not have access to this directory, and consequently, applications that use ADSI interfaces that are run in this mode will download the schema on every connection, which will impact throughput and performance.</span></span>

<span data-ttu-id="5d0ee-111">**Soluções**</span><span class="sxs-lookup"><span data-stu-id="5d0ee-111">**Solutions**</span></span>

<span data-ttu-id="5d0ee-112">*Usuário único* – para resolver esse problema, há novas chaves de controle do registro de provedor ADSI que determinam os locais de registro e os locais de arquivo para objetos de [esquema de Active Directory](/windows/desktop/ADSchema/active-directory-schema) em cache.</span><span class="sxs-lookup"><span data-stu-id="5d0ee-112">*Single user* - To resolve this issue, there are new ADSI Provider registry control keys that determine the registry locations and file locations for cached [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) objects.</span></span> <span data-ttu-id="5d0ee-113">Se a chave do registro</span><span class="sxs-lookup"><span data-stu-id="5d0ee-113">If the registry key</span></span>

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

<span data-ttu-id="5d0ee-114">é definido como 0 (zero), cada usuário terá um local de armazenamento diferente para ADSI; as chaves do registro serão armazenadas em</span><span class="sxs-lookup"><span data-stu-id="5d0ee-114">is set to 0 (zero), each user will have a different storage location for ADSI; registry keys will be stored in</span></span>

`HKEY_CURRENT_USER\Software\Microsoft\ADs\Providers\LDAP\`

<span data-ttu-id="5d0ee-115">e os arquivos de cache serão armazenados em</span><span class="sxs-lookup"><span data-stu-id="5d0ee-115">and cache files will be stored in</span></span>

`%LOCALAPPDATA%\Microsoft\Windows\SchCache`

<span data-ttu-id="5d0ee-116">Essas configurações são as configurações padrão em computadores que executam o Windows Server 2008 ou o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5d0ee-116">These settings are the default settings on computers running Windows Server 2008 or Windows Vista.</span></span>

<span data-ttu-id="5d0ee-117">*Multiusuário* – se você estiver executando aplicativos ADSI em um computador com muitas contas de usuário (por exemplo, um servidor Web), é preferível não ter muitas cópias do cache de [esquema de Active Directory](/windows/desktop/ADSchema/active-directory-schema) usando grandes quantidades de espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="5d0ee-117">*Multi-user* - If you are running ADSI applications on a computer with many user accounts (for example, a web server), then it's preferable not to have many copies of the [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) cache using up large amounts of disk space.</span></span> <span data-ttu-id="5d0ee-118">Configurando a chave do registro</span><span class="sxs-lookup"><span data-stu-id="5d0ee-118">Setting the registry key</span></span>

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

<span data-ttu-id="5d0ee-119">para 1 (um), o ADSI será revertido para o comportamento anterior; todos os objetos de [esquema de Active Directory](/windows/desktop/ADSchema/active-directory-schema) serão armazenados em seus locais anteriores; a chave do registro estará em</span><span class="sxs-lookup"><span data-stu-id="5d0ee-119">to 1 (one) will revert ADSI to the previous behavior; all [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) objects will be stored in their previous locations; the registry key will be in</span></span>

`HKEY_LOCAL_MACHINE\Software\Microsoft\ADs\Providers\LDAP`

<span data-ttu-id="5d0ee-120">e o arquivo de cache estará em</span><span class="sxs-lookup"><span data-stu-id="5d0ee-120">and the cache file will be in</span></span>

`%systemroot%\SchCache`

<span data-ttu-id="5d0ee-121">Nesse caso, as contas de administrador devem executar o aplicativo, o que fará com que o arquivo de esquema seja armazenado em cache no local global para uso futuro pelos usuários menos privilegiados.</span><span class="sxs-lookup"><span data-stu-id="5d0ee-121">In this case, administrator accounts should run the application, which will cause the schema file to be cached in the global location for future use by the less privileged users.</span></span>

 

 
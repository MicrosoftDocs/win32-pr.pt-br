---
title: Restaurando objetos excluídos
description: O Windows Server 2003 inclui o \ 0034; restaurar objetos excluídos \ 0034; recurso.
ms.assetid: b64c5c91-fb76-4323-b78d-f692aa887c96
ms.tgt_platform: multiple
keywords:
- Restaurando o AD de objetos excluídos
- Active Directory, usando, restaurando objetos excluídos
- AD de objetos, restaurando objetos excluídos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f8f1d3511bb4246826e677aa239ca594918127a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104499016"
---
# <a name="restoring-deleted-objects"></a><span data-ttu-id="59e3d-106">Restaurando objetos excluídos</span><span class="sxs-lookup"><span data-stu-id="59e3d-106">Restoring Deleted Objects</span></span>

<span data-ttu-id="59e3d-107">O Windows Server 2003 inclui o recurso "restaurar objetos excluídos".</span><span class="sxs-lookup"><span data-stu-id="59e3d-107">Windows Server 2003 includes the "restore deleted objects" feature.</span></span>

<span data-ttu-id="59e3d-108">Para habilitar a restauração de objeto excluído, pelo menos um controlador de domínio no domínio deve estar em execução no Windows Server 2003 ou em uma versão posterior do Windows.</span><span class="sxs-lookup"><span data-stu-id="59e3d-108">To enable deleted object restoration, at least one domain controller in the domain must be running on Windows Server 2003 or a later version of Windows.</span></span> <span data-ttu-id="59e3d-109">Por padrão, somente os administradores de domínio podem restaurar objetos excluídos, embora isso possa ser delegado a outras pessoas.</span><span class="sxs-lookup"><span data-stu-id="59e3d-109">By default, only domain administrators can restore deleted objects, though this can be delegated to others.</span></span>

<span data-ttu-id="59e3d-110">As seguintes limitações se aplicam à restauração de objetos excluídos:</span><span class="sxs-lookup"><span data-stu-id="59e3d-110">The following limitations apply to restoring deleted objects:</span></span>

-   <span data-ttu-id="59e3d-111">Não é possível restaurar um objeto quando o tempo de vida da marca para exclusão do objeto expirou porque, quando o tempo de vida da marca para exclusão expirou, o objeto é excluído permanentemente.</span><span class="sxs-lookup"><span data-stu-id="59e3d-111">An object cannot be restored when the tombstone lifetime for the object has expired because when the tombstone lifetime has expired, the object is permanently deleted.</span></span>
-   <span data-ttu-id="59e3d-112">Os objetos que existem na raiz do contexto de nomenclatura, como uma partição de aplicativo ou de domínio, não podem ser restaurados.</span><span class="sxs-lookup"><span data-stu-id="59e3d-112">Objects that exist at the root of the naming context, such as a domain or application partition, cannot be restored.</span></span>
-   <span data-ttu-id="59e3d-113">Objetos de esquema não podem ser restaurados.</span><span class="sxs-lookup"><span data-stu-id="59e3d-113">Schema objects cannot be restored.</span></span> <span data-ttu-id="59e3d-114">Os objetos de esquema nunca devem ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="59e3d-114">Schema objects should never be deleted.</span></span>
-   <span data-ttu-id="59e3d-115">É possível restaurar os contêineres excluídos, mas a restauração dos objetos excluídos que estavam no contêiner antes da exclusão é difícil porque a estrutura de árvore no contêiner deve ser reconstruída manualmente.</span><span class="sxs-lookup"><span data-stu-id="59e3d-115">It is possible to restore deleted containers, but the restoration of the deleted objects that were in the container before the deletion is difficult because the tree structure under the container must be manually reconstructed.</span></span>

## <a name="permissions-required-to-restore-a-deleted-object"></a><span data-ttu-id="59e3d-116">Permissões necessárias para restaurar um objeto excluído</span><span class="sxs-lookup"><span data-stu-id="59e3d-116">Permissions Required to Restore a Deleted Object</span></span>

<span data-ttu-id="59e3d-117">Quando um objeto é excluído, o descritor de segurança do objeto é mantido.</span><span class="sxs-lookup"><span data-stu-id="59e3d-117">When an object is deleted, the object security descriptor is retained.</span></span> <span data-ttu-id="59e3d-118">Embora o proprietário seja identificável a partir do descritor de segurança, por motivos de segurança, somente administradores de domínio têm permissão para restaurar objetos excluídos.</span><span class="sxs-lookup"><span data-stu-id="59e3d-118">Although the owner is identifiable from the security descriptor, for security reasons, only domain administrators are allowed to restore deleted objects.</span></span> <span data-ttu-id="59e3d-119">Os administradores de domínio podem conceder a permissão para restaurar objetos de exclusão para outros usuários e grupos concedendo ao usuário ou grupo o direito de acesso de controle "reanimar a marca para exclusão".</span><span class="sxs-lookup"><span data-stu-id="59e3d-119">Domain administrators can grant the permission to restore delete objects to other users and groups by granting the user or group the "Reanimate Tombstone" control access right.</span></span> <span data-ttu-id="59e3d-120">O direito de acesso de controle "reanimar marca para exclusão" é concedido na raiz do contexto de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="59e3d-120">The "Reanimate Tombstone" control access right is granted at the Naming Context root.</span></span> <span data-ttu-id="59e3d-121">Somente os usuários que tinham permissão de acesso de leitura em um objeto e seus atributos terão permissão para ler o objeto e os atributos acessíveis depois que o objeto for excluído.</span><span class="sxs-lookup"><span data-stu-id="59e3d-121">Only users that had read access permission on an object and its attributes are permitted to read the object and accessible attributes after the object is deleted.</span></span>

> [!Note]  
> <span data-ttu-id="59e3d-122">Conceder a um usuário essa permissão pode ser um risco de segurança, pois ela pode permitir que o usuário restaure um objeto de conta que tenha acesso aos recursos aos quais o usuário normalmente não teria acesso.</span><span class="sxs-lookup"><span data-stu-id="59e3d-122">Granting a user this permission can be a security risk because it could permit the user to restore an account object that has access to resources that the user would not normally have access to.</span></span> <span data-ttu-id="59e3d-123">Ao restaurar uma conta, o usuário essencialmente Obtém o controle dessa conta, pois o usuário deve definir a senha inicial na conta quando a conta é restaurada.</span><span class="sxs-lookup"><span data-stu-id="59e3d-123">By restoring an account, the user essentially gains control of this account because the user must set the initial password on the account when the account is restored.</span></span>

 

<span data-ttu-id="59e3d-124">Para restaurar completamente um objeto excluído, o usuário deve:</span><span class="sxs-lookup"><span data-stu-id="59e3d-124">To completely restore a deleted object, the user must:</span></span>

-   <span data-ttu-id="59e3d-125">Ter ou ser membro de um grupo que tenha o direito de acesso de controle "reanimar marca de exclusão".</span><span class="sxs-lookup"><span data-stu-id="59e3d-125">Have, or be a member of a group that has, the "Reanimate Tombstone" control access right.</span></span>

-   <span data-ttu-id="59e3d-126">Ter acesso de gravação para cada atributo obrigatório que requer atualização.</span><span class="sxs-lookup"><span data-stu-id="59e3d-126">Have write access for each mandatory attribute that requires updating.</span></span>

-   <span data-ttu-id="59e3d-127">Ter acesso de gravação ao nome distinto relativo (RDN).</span><span class="sxs-lookup"><span data-stu-id="59e3d-127">Have write access to the Relative Distinguished Name (RDN).</span></span>

-   <span data-ttu-id="59e3d-128">Ter acesso de gravação para cada atributo opcional que precisa ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="59e3d-128">Have write access to each optional attribute that needs to be updated.</span></span>

-   <span data-ttu-id="59e3d-129">Ter direitos de criação de filho no contêiner de destino para a classe de objeto do objeto restaurado.</span><span class="sxs-lookup"><span data-stu-id="59e3d-129">Have child-creation rights on the destination container for the object class of restored object.</span></span>

    > [!Note]  
    > <span data-ttu-id="59e3d-130">O atributo **IsDeleted** não é verificado durante a operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="59e3d-130">The **isDeleted** attribute is not verified during the restore operation.</span></span> <span data-ttu-id="59e3d-131">Nenhuma permissão DELETE-filho no contêiner "objetos excluídos" será verificada.</span><span class="sxs-lookup"><span data-stu-id="59e3d-131">Neither will the delete-child permission on the "Deleted Objects" container be verified.</span></span>

     

## <a name="restoring-a-deleted-object"></a><span data-ttu-id="59e3d-132">Restaurando um objeto excluído</span><span class="sxs-lookup"><span data-stu-id="59e3d-132">Restoring a Deleted Object</span></span>

<span data-ttu-id="59e3d-133">Para restaurar um objeto excluído, primeiro o objeto deve estar localizado no contêiner objetos excluídos.</span><span class="sxs-lookup"><span data-stu-id="59e3d-133">To restore a deleted object, the object must first be located in the Deleted Objects container.</span></span> <span data-ttu-id="59e3d-134">Para obter mais informações sobre como recuperar objetos excluídos, consulte [recuperando objetos excluídos](retrieving-deleted-objects.md).</span><span class="sxs-lookup"><span data-stu-id="59e3d-134">For more information about retrieving deleted objects, see [Retrieving Deleted Objects](retrieving-deleted-objects.md).</span></span>

<span data-ttu-id="59e3d-135">Quando o objeto estiver localizado, as operações a seguir devem ser concluídas em uma única operação LDAP.</span><span class="sxs-lookup"><span data-stu-id="59e3d-135">When the object has been located, the following operations must be completed in a single LDAP operation.</span></span> <span data-ttu-id="59e3d-136">Isso requer o uso da função [**LDAP \_ Modify \_ ext \_**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) com o [**servidor LDAP mostrar controle de \_ \_ \_ \_ OID excluído**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) .</span><span class="sxs-lookup"><span data-stu-id="59e3d-136">This requires the use of the [**ldap\_modify\_ext\_s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) function with the [**LDAP\_SERVER\_SHOW\_DELETED\_OID**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) control.</span></span>

-   <span data-ttu-id="59e3d-137">Remova o valor do atributo **IsDeleted** .</span><span class="sxs-lookup"><span data-stu-id="59e3d-137">Remove the **isDeleted** attribute value.</span></span> <span data-ttu-id="59e3d-138">O valor do atributo **IsDeleted** deve ser removido, não definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="59e3d-138">The **isDeleted** attribute value must be removed, not set to **FALSE**.</span></span>
-   <span data-ttu-id="59e3d-139">Substitua o nome distinto do objeto para que ele seja movido para um contêiner diferente do contêiner objetos excluídos.</span><span class="sxs-lookup"><span data-stu-id="59e3d-139">Replace the distinguished name of the object so that it is moved to a container other than the Deleted Objects container.</span></span> <span data-ttu-id="59e3d-140">Pode ser qualquer contêiner que normalmente possa conter o objeto.</span><span class="sxs-lookup"><span data-stu-id="59e3d-140">This can be any container that can normally contain the object.</span></span> <span data-ttu-id="59e3d-141">O nome distinto do contêiner anterior do objeto pode ser encontrado no atributo **lastKnownParent** do objeto excluído.</span><span class="sxs-lookup"><span data-stu-id="59e3d-141">The distinguished name of the previous container of the object can be found in the deleted object's **lastKnownParent** attribute.</span></span> <span data-ttu-id="59e3d-142">O atributo **lastKnownParent** só será definido se o objeto tiver sido excluído em um controlador de domínio do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="59e3d-142">The **lastKnownParent** attribute is only set if the object was deleted on a Windows Server 2003 domain controller.</span></span> <span data-ttu-id="59e3d-143">Portanto, é possível que o conteúdo do atributo **lastKnownParent** seja impreciso.</span><span class="sxs-lookup"><span data-stu-id="59e3d-143">Thus, it is possible that the content of the **lastKnownParent** attribute is inaccurate.</span></span>
-   <span data-ttu-id="59e3d-144">Restaure os atributos obrigatórios para o objeto que foram limpos durante a exclusão.</span><span class="sxs-lookup"><span data-stu-id="59e3d-144">Restore the mandatory attributes for the object that were cleared during deletion.</span></span>

> [!Note]  
> <span data-ttu-id="59e3d-145">O atributo **objectCategory** também pode ser definido quando o objeto é restaurado, mas não é necessário.</span><span class="sxs-lookup"><span data-stu-id="59e3d-145">The **objectCategory** attribute can also be set when the object is restored, but is not required.</span></span> <span data-ttu-id="59e3d-146">Se nenhum valor **objectCategory** for especificado, o **objectCategory** padrão para o **objectClass** do objeto será usado.</span><span class="sxs-lookup"><span data-stu-id="59e3d-146">If no **objectCategory** value is specified, the default **objectCategory** for the object's **objectClass** is used.</span></span>

 

<span data-ttu-id="59e3d-147">Depois que o objeto é restaurado, ele pode ser acessado como era antes de ser excluído.</span><span class="sxs-lookup"><span data-stu-id="59e3d-147">After the object is restored, it can be accessed as it was before it was deleted.</span></span> <span data-ttu-id="59e3d-148">Neste ponto, todos os atributos opcionais que são importantes devem ser restaurados.</span><span class="sxs-lookup"><span data-stu-id="59e3d-148">At this point, any optional attributes that are important should be restored.</span></span> <span data-ttu-id="59e3d-149">Todas as referências ao objeto de outros objetos no diretório também devem ser restauradas.</span><span class="sxs-lookup"><span data-stu-id="59e3d-149">Any references to the object from other objects in the directory must also be restored.</span></span>

<span data-ttu-id="59e3d-150">Como medida de segurança, os objetos de usuário são desabilitados quando são restaurados.</span><span class="sxs-lookup"><span data-stu-id="59e3d-150">As a security measure, user objects are disabled when they are restored.</span></span> <span data-ttu-id="59e3d-151">Os objetos de usuário devem ser habilitados após a restauração dos atributos opcionais para permitir que o objeto de usuário seja usado.</span><span class="sxs-lookup"><span data-stu-id="59e3d-151">User objects must be enabled after restoring the optional attributes to allow the user object to be used.</span></span>

<span data-ttu-id="59e3d-152">Para obter mais informações e um exemplo de código que mostra como restaurar um objeto excluído, consulte a função RestoreDeletedObject abaixo.</span><span class="sxs-lookup"><span data-stu-id="59e3d-152">For more information and a code example that shows how to restore a deleted object, see the RestoreDeletedObject function below.</span></span>

## <a name="restoredeletedobject"></a><span data-ttu-id="59e3d-153">RestoreDeletedObject</span><span class="sxs-lookup"><span data-stu-id="59e3d-153">RestoreDeletedObject</span></span>

<span data-ttu-id="59e3d-154">O exemplo de código C++ a seguir mostra como restaurar um objeto excluído.</span><span class="sxs-lookup"><span data-stu-id="59e3d-154">The following C++ code example shows how to restore a deleted object.</span></span>


```C++
//***************************************************************************
//
//  RestoreDeletedObject()
//
//  Restores a deleted object. 
//
//  pwszDeletedDN - Contains the fully qualified distinguished name of the 
//  deleted object.
//
//  pwszDestContainerDN - Contains the fully qualified distinguished name of 
//  the folder that the deleted object should be moved to.
//
//  Returns S_OK if successful or an HRESULT or LDAP error code otherwise.
//
//***************************************************************************

HRESULT RestoreDeletedObject(LPCWSTR pwszDeletedDN, LPCWSTR pwszDestContainerDN)
{
    if((NULL == pwszDeletedDN) || (NULL == pwszDestContainerDN))
    {
        return E_POINTER;
    }
    
    HRESULT hr = E_FAIL;

    // Build the new distinguished name.
    LPWSTR pwszNewDN = new WCHAR[lstrlenW(pwszDeletedDN) + lstrlenW(pwszDestContainerDN) + 1];
    if(pwszNewDN)
    {
        wcscpy_s(pwszNewDN, pwszDeletedDN);

        // Search for the first 0x0A character. This is the delimiter in the deleted object name.
        LPWSTR pwszChar;
        for(pwszChar = pwszNewDN; *pwszChar; pwszChar = CharNextW(pwszChar))
        {
            if(('\\' == *pwszChar) && ('0' == *(pwszChar + 1)) && ('A' == *(pwszChar + 2)))
            {
                break;
            }
            
        }

        if(0 != *pwszChar)
        {
            // Truncate the name string at the delimiter.
            *pwszChar = 0;

            // Add the last known parent DN to complete the DN.
            wcscat_s(pwszNewDN, L",");
            wcscat_s(pwszNewDN, pwszDestContainerDN);

            PLDAP ld;

            // Initialize LDAP.
            ld = ldap_init(NULL, LDAP_PORT);
            if(NULL != ld) 
            {
                ULONG ulRC;
                ULONG version = LDAP_VERSION3;

                // Set the LDAP version.
                ulRC = ldap_set_option(ld, LDAP_OPT_PROTOCOL_VERSION, (void*)&version);
                if(LDAP_SUCCESS == ulRC)
                {
                    // Establish a connection with the server.
                    ulRC = ldap_connect(ld, NULL);
                    if(LDAP_SUCCESS == ulRC)
                    {                    
                        // Bind to the LDAP server.
                        ulRC = ldap_bind_s(ld, NULL, NULL, LDAP_AUTH_NEGOTIATE);
                        if(LDAP_SUCCESS == ulRC)
                        {
                            // Setup the new values.
                            LPWSTR rgNewVals[] = {pwszNewDN, NULL};

                            /*
                            Remove the isDeleted attribute. This cannot be set 
                            to FALSE or the restore operation will not work.
                            */
                            LDAPModW modIsDeleted = { LDAP_MOD_DELETE, L"isDeleted", NULL };

                            /*
                            Set the new DN, in effect, moving the deleted 
                            object to where it resided before the deletion.
                            */
                            LDAPModW modDN = { LDAP_MOD_REPLACE, L"distinguishedName", rgNewVals };
                            
                            // Initialize the LDAPMod structure.
                            PLDAPModW ldapMods[] = 
                            {
                                &modIsDeleted,
                                &modDN,
                                NULL
                            };

                            /*
                            Use the LDAP_SERVER_SHOW_DELETED_OID control to 
                            modify deleted objects.
                            */
                            LDAPControlW showDeletedControl;
                            showDeletedControl.ldctl_oid = LDAP_SERVER_SHOW_DELETED_OID_W;
                            showDeletedControl.ldctl_value.bv_len = 0;
                            showDeletedControl.ldctl_value.bv_val = NULL;
                            showDeletedControl.ldctl_iscritical = TRUE;

                            // Initialzie the LDAPControl structure
                            PLDAPControlW ldapControls[] = { &showDeletedControl, NULL };

                            /*
                            Modify the specified attributes. This must performed 
                            in one step, which is why the LDAP APIs must be used 
                            to restore a deleted object.
                            */
                            ulRC = ldap_modify_ext_sW(ld, (PWCHAR)pwszDeletedDN, ldapMods, ldapControls, NULL);
                            if(LDAP_SUCCESS == ulRC)
                            {
                                hr = S_OK;
                            }
                            else if(LDAP_ALREADY_EXISTS == ulRC)
                            {
                                /*
                                An object already exists with the specified name 
                                in the specified target container. At this point, 
                                a new name must be selected.
                                */
                            }
                        }
                    }
                }

                if(LDAP_SUCCESS != ulRC)
                {
                    hr = ulRC;
                    
                    OutputDebugString(ldap_err2string(ulRC));
                }

                // Release the LDAP session.
                ldap_unbind(ld);
            }
        }
        else
        {
            /*
            If the end of the string is reached before the delimiter is found, just 
            end and fail.
            */
            hr = E_INVALIDARG;
        }
    
        delete pwszNewDN;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }

    return hr;
}

```



 

 
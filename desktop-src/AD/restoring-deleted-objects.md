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
# <a name="restoring-deleted-objects"></a>Restaurando objetos excluídos

O Windows Server 2003 inclui o recurso "restaurar objetos excluídos".

Para habilitar a restauração de objeto excluído, pelo menos um controlador de domínio no domínio deve estar em execução no Windows Server 2003 ou em uma versão posterior do Windows. Por padrão, somente os administradores de domínio podem restaurar objetos excluídos, embora isso possa ser delegado a outras pessoas.

As seguintes limitações se aplicam à restauração de objetos excluídos:

-   Não é possível restaurar um objeto quando o tempo de vida da marca para exclusão do objeto expirou porque, quando o tempo de vida da marca para exclusão expirou, o objeto é excluído permanentemente.
-   Os objetos que existem na raiz do contexto de nomenclatura, como uma partição de aplicativo ou de domínio, não podem ser restaurados.
-   Objetos de esquema não podem ser restaurados. Os objetos de esquema nunca devem ser excluídos.
-   É possível restaurar os contêineres excluídos, mas a restauração dos objetos excluídos que estavam no contêiner antes da exclusão é difícil porque a estrutura de árvore no contêiner deve ser reconstruída manualmente.

## <a name="permissions-required-to-restore-a-deleted-object"></a>Permissões necessárias para restaurar um objeto excluído

Quando um objeto é excluído, o descritor de segurança do objeto é mantido. Embora o proprietário seja identificável a partir do descritor de segurança, por motivos de segurança, somente administradores de domínio têm permissão para restaurar objetos excluídos. Os administradores de domínio podem conceder a permissão para restaurar objetos de exclusão para outros usuários e grupos concedendo ao usuário ou grupo o direito de acesso de controle "reanimar a marca para exclusão". O direito de acesso de controle "reanimar marca para exclusão" é concedido na raiz do contexto de nomenclatura. Somente os usuários que tinham permissão de acesso de leitura em um objeto e seus atributos terão permissão para ler o objeto e os atributos acessíveis depois que o objeto for excluído.

> [!Note]  
> Conceder a um usuário essa permissão pode ser um risco de segurança, pois ela pode permitir que o usuário restaure um objeto de conta que tenha acesso aos recursos aos quais o usuário normalmente não teria acesso. Ao restaurar uma conta, o usuário essencialmente Obtém o controle dessa conta, pois o usuário deve definir a senha inicial na conta quando a conta é restaurada.

 

Para restaurar completamente um objeto excluído, o usuário deve:

-   Ter ou ser membro de um grupo que tenha o direito de acesso de controle "reanimar marca de exclusão".

-   Ter acesso de gravação para cada atributo obrigatório que requer atualização.

-   Ter acesso de gravação ao nome distinto relativo (RDN).

-   Ter acesso de gravação para cada atributo opcional que precisa ser atualizado.

-   Ter direitos de criação de filho no contêiner de destino para a classe de objeto do objeto restaurado.

    > [!Note]  
    > O atributo **IsDeleted** não é verificado durante a operação de restauração. Nenhuma permissão DELETE-filho no contêiner "objetos excluídos" será verificada.

     

## <a name="restoring-a-deleted-object"></a>Restaurando um objeto excluído

Para restaurar um objeto excluído, primeiro o objeto deve estar localizado no contêiner objetos excluídos. Para obter mais informações sobre como recuperar objetos excluídos, consulte [recuperando objetos excluídos](retrieving-deleted-objects.md).

Quando o objeto estiver localizado, as operações a seguir devem ser concluídas em uma única operação LDAP. Isso requer o uso da função [**LDAP \_ Modify \_ ext \_**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) com o [**servidor LDAP mostrar controle de \_ \_ \_ \_ OID excluído**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) .

-   Remova o valor do atributo **IsDeleted** . O valor do atributo **IsDeleted** deve ser removido, não definido como **false**.
-   Substitua o nome distinto do objeto para que ele seja movido para um contêiner diferente do contêiner objetos excluídos. Pode ser qualquer contêiner que normalmente possa conter o objeto. O nome distinto do contêiner anterior do objeto pode ser encontrado no atributo **lastKnownParent** do objeto excluído. O atributo **lastKnownParent** só será definido se o objeto tiver sido excluído em um controlador de domínio do Windows Server 2003. Portanto, é possível que o conteúdo do atributo **lastKnownParent** seja impreciso.
-   Restaure os atributos obrigatórios para o objeto que foram limpos durante a exclusão.

> [!Note]  
> O atributo **objectCategory** também pode ser definido quando o objeto é restaurado, mas não é necessário. Se nenhum valor **objectCategory** for especificado, o **objectCategory** padrão para o **objectClass** do objeto será usado.

 

Depois que o objeto é restaurado, ele pode ser acessado como era antes de ser excluído. Neste ponto, todos os atributos opcionais que são importantes devem ser restaurados. Todas as referências ao objeto de outros objetos no diretório também devem ser restauradas.

Como medida de segurança, os objetos de usuário são desabilitados quando são restaurados. Os objetos de usuário devem ser habilitados após a restauração dos atributos opcionais para permitir que o objeto de usuário seja usado.

Para obter mais informações e um exemplo de código que mostra como restaurar um objeto excluído, consulte a função RestoreDeletedObject abaixo.

## <a name="restoredeletedobject"></a>RestoreDeletedObject

O exemplo de código C++ a seguir mostra como restaurar um objeto excluído.


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



 

 
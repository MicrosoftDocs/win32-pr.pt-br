---
description: Um aplicativo pode chamar as funções MsiEnumProducts ou MsiEnumProductsEx para enumerar os produtos que estão instalados ou anunciados no sistema.
ms.assetid: 162bda20-0c62-4eac-8c1f-fd107e42c528
title: Determinando o contexto de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c3ea847a410c5d253061e93153da4462e3cdd8ae8da12b4b6b701812d37d89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764256"
---
# <a name="determining-installation-context"></a>Determinando o contexto de instalação

Um aplicativo pode chamar as funções [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) ou [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) para enumerar os produtos que estão instalados ou anunciados no sistema. Essa função pode enumerar todos os produtos instalados no [contexto de instalação](installation-context.md)por máquina. Ele pode enumerar os produtos instalados no contexto por usuário para o usuário atual. O aplicativo pode recuperar informações sobre o contexto desses produtos chamando as funções [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) ou [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) .

o Windows Installer pode instalar produtos para serem executados com privilégios elevados (sistema) para usuários não administradores. Isso requer a permissão de um usuário administrador. Um produto que é instalado com privilégios elevados é chamado de "gerenciado". Todos os produtos instalados por computador são gerenciados. Os produtos instalados por usuário só serão gerenciados se um agente do sistema local executar um anúncio ao representar um usuário. Esse é o método usado pela implantação de software por meio de [política de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page). Aplicativos por usuário instalados enquanto as políticas de [AlwaysInstallElevated](alwaysinstallelevated.md) são definidas não são considerados gerenciados. Ao chamar [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda), um aplicativo pode verificar se um produto específico é gerenciado.

O exemplo a seguir demonstra como um aplicativo determina o contexto usando [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa), [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)e [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda).


```C++
#ifndef UNICODE
#define UNICODE
#endif //UNICODE

#ifndef _WIN32_MSI
#define _WIN32_MSI 200
#endif //_WIN32_MSI

#include <stdio.h>
#include <windows.h>
#include <msi.h>
#pragma comment(lib, "msi.lib")

const int cchGUID = 38;

UINT DetermineContextForAllProducts()
{
    WCHAR wszProductCode[cchGUID+1] = {0};
    WCHAR wszAssignmentType[10] = {0};
    DWORD cchAssignmentType = 
            sizeof(wszAssignmentType)/sizeof(wszAssignmentType[0]);
    DWORD dwIndex = 0;

    DWORD cchProductName = MAX_PATH;
    WCHAR* lpProductName = new WCHAR[cchProductName];
    if (!lpProductName)
    {
        return ERROR_OUTOFMEMORY;
    }

    UINT uiStatus = ERROR_SUCCESS;

    // enumerate all visible products
    do
    {
        uiStatus = MsiEnumProducts(dwIndex,
                          wszProductCode);
        if (ERROR_SUCCESS == uiStatus)
        {
            cchAssignmentType = 
                sizeof(wszAssignmentType)/sizeof(wszAssignmentType[0]);
            BOOL fPerMachine = FALSE;
            BOOL fManaged = FALSE;

            // Determine assignment type of product
            // This indicates whether the product
            // instance is per-user or per-machine
            if (ERROR_SUCCESS == 
                MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_ASSIGNMENTTYPE,wszAssignmentType,&cchAssignmentType))
            {
                if (L'1' == wszAssignmentType[0])
                    fPerMachine = TRUE;
            }
            else
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // determine the "managed" status of the product.
            // If fManaged is TRUE, product is installed managed
            // and runs with elevated privileges.
            // If fManaged is FALSE, product installation operations
            // run as the user.
            if (ERROR_SUCCESS != MsiIsProductElevated(wszProductCode,
                                         &fManaged))
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // obtain the user friendly name of the product
            UINT uiReturn = MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_PRODUCTNAME,lpProductName,&cchProductName);
            if (ERROR_MORE_DATA == uiReturn)
            {
                // try again, but with a larger product name buffer
                delete [] lpProductName;

                // returned character count does not include
                // terminating NULL
                ++cchProductName;

                lpProductName = new WCHAR[cchProductName];
                if (!lpProductName)
                {
                    uiStatus = ERROR_OUTOFMEMORY;
                    break;
                }

                uiReturn = MsiGetProductInfo(wszProductCode,INSTALLPROPERTY_PRODUCTNAME,lpProductName,&cchProductName);
            }

            if (ERROR_SUCCESS != uiReturn)
            {
                // This halts the enumeration and fails. Alternatively the error
                // could be logged and enumeration continued for the
                // remainder of the products
                uiStatus = ERROR_FUNCTION_FAILED;
                break;
            }

            // output information
            wprintf(L" Product %s:\n", lpProductName);
            wprintf(L"\t%s\n", wszProductCode);
                        wprintf(L"\tInstalled %s %s\n", 
                fPerMachine ? L"per-machine" : L"per-user",
                fManaged ? L"managed" : L"non-managed");
        }
        dwIndex++;
    }
    while (ERROR_SUCCESS == uiStatus);

    if (lpProductName)
    {
        delete [] lpProductName;
        lpProductName = NULL;
    }

    return (ERROR_NO_MORE_ITEMS == uiStatus) ? ERROR_SUCCESS : uiStatus;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> <dt>

[**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)
</dt> <dt>

[**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)
</dt> <dt>

[Instalando um pacote com privilégios elevados para um não administrador](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
</dt> <dt>

[Anunciando um aplicativo Per-User para ser instalado com privilégios elevados](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
</dt> <dt>

[Contexto de instalação](installation-context.md)
</dt> </dl>

 

 

---
title: Alterando elementos de informações do usuário
description: As funções de gerenciamento de rede fornecem uma variedade de níveis de informações para ajudar a alterar as informações do usuário.
ms.assetid: dc126431-57b0-467b-9f56-1e66a647c7b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e1aa6ec8d7fed30d38d25adc67974d8bad8ab1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105757762"
---
# <a name="changing-elements-of-user-information"></a><span data-ttu-id="80a8b-103">Alterando elementos de informações do usuário</span><span class="sxs-lookup"><span data-stu-id="80a8b-103">Changing Elements of User Information</span></span>

<span data-ttu-id="80a8b-104">As funções de gerenciamento de rede fornecem uma variedade de níveis de informações para ajudar a alterar as informações do usuário.</span><span class="sxs-lookup"><span data-stu-id="80a8b-104">The network management functions provide a variety of information levels to assist in changing user information.</span></span> <span data-ttu-id="80a8b-105">Alguns níveis exigem privilégios administrativos para serem executados com êxito.</span><span class="sxs-lookup"><span data-stu-id="80a8b-105">Some levels require administrative privileges to execute successfully.</span></span> <span data-ttu-id="80a8b-106">Para obter mais informações sobre como chamar funções que exigem privilégios de administrador, consulte [executando com privilégios especiais](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="80a8b-106">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="80a8b-107">O código de exemplo neste tópico demonstra como alterar vários elementos de informações do usuário chamando a função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="80a8b-107">The sample code in this topic demonstrates how to change several elements of user information by calling the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="80a8b-108">O código usa várias estruturas de informações de gerenciamento de rede.</span><span class="sxs-lookup"><span data-stu-id="80a8b-108">The code uses various network management information structures.</span></span>

<span data-ttu-id="80a8b-109">Ao alterar as informações do usuário, é melhor usar o nível específico para essa informação.</span><span class="sxs-lookup"><span data-stu-id="80a8b-109">When changing user information, it is best to use the specific level for that piece of information.</span></span> <span data-ttu-id="80a8b-110">Isso impede a redefinição acidental de informações não relacionadas ao usar os valores de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="80a8b-110">This prevents the accidental resetting of unrelated information when using the lower level values.</span></span>

<span data-ttu-id="80a8b-111">Definir alguns dos níveis mais comumente usados é ilustrado nos exemplos de código a seguir:</span><span class="sxs-lookup"><span data-stu-id="80a8b-111">Setting some of the more commonly used levels is illustrated in the following code samples:</span></span>

-   [<span data-ttu-id="80a8b-112">Definindo a senha do usuário, nível 1003</span><span class="sxs-lookup"><span data-stu-id="80a8b-112">Setting the User Password, Level 1003</span></span>](#setting-the-user-password-level-1003)
-   [<span data-ttu-id="80a8b-113">Configurando o privilégio de usuário, nível 1005</span><span class="sxs-lookup"><span data-stu-id="80a8b-113">Setting the User Privilege, Level 1005</span></span>](#setting-the-user-privilege-level-1005)
-   [<span data-ttu-id="80a8b-114">Configurando o diretório base do usuário, nível 1006</span><span class="sxs-lookup"><span data-stu-id="80a8b-114">Setting the User Home Directory, Level 1006</span></span>](#setting-the-user-home-directory-level-1006)
-   [<span data-ttu-id="80a8b-115">Configurando o campo comentário do usuário, nível 1007</span><span class="sxs-lookup"><span data-stu-id="80a8b-115">Setting the User Comment Field, Level 1007</span></span>](#setting-the-user-comment-field-level-1007)
-   [<span data-ttu-id="80a8b-116">Configurando os sinalizadores de usuário, nível 1008</span><span class="sxs-lookup"><span data-stu-id="80a8b-116">Setting the User Flags, Level 1008</span></span>](#setting-the-user-flags-level-1008)
-   [<span data-ttu-id="80a8b-117">Configurando o caminho do script do usuário, nível 1009</span><span class="sxs-lookup"><span data-stu-id="80a8b-117">Setting the User Script Path, Level 1009</span></span>](#setting-the-user-script-path-level-1009)
-   [<span data-ttu-id="80a8b-118">Configurando os sinalizadores de autoridade de usuário, nível 1010</span><span class="sxs-lookup"><span data-stu-id="80a8b-118">Setting The User Authority Flags, Level 1010</span></span>](#setting-the-user-authority-flags-level-1010)
-   [<span data-ttu-id="80a8b-119">Definindo o nome completo do usuário, nível 1011</span><span class="sxs-lookup"><span data-stu-id="80a8b-119">Setting The User Full Name, Level 1011</span></span>](#setting-the-user-full-name-level-1011)

<span data-ttu-id="80a8b-120">Todos os fragmentos de código pressupõem que o usuário definiu a diretiva de compilação UNICODE e incluiu os arquivos de cabeçalho do SDK apropriados, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="80a8b-120">All code fragments assume that the user has defined the UNICODE compile directive and included the appropriate SDK header files, as follows:</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#define INCL_NET
#include <lm.h>
#include <stdio.h>

#pragma comment(lib, "netapi32.lib")

#define SERVER L"test_server_name"
#define USERNAME L"test_user_name"

DWORD netRet = 0;
```



## <a name="setting-the-user-password-level-1003"></a><span data-ttu-id="80a8b-121">Definindo a senha do usuário, nível 1003</span><span class="sxs-lookup"><span data-stu-id="80a8b-121">Setting the User Password, Level 1003</span></span>

<span data-ttu-id="80a8b-122">O fragmento de código a seguir ilustra como definir a senha de um usuário com um valor conhecido com uma chamada para a função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="80a8b-122">The following code fragment illustrates how to set a user's password to a known value with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="80a8b-123">O [**tópico \_ informações \_ do usuário 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) contém informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="80a8b-123">The [**USER\_INFO\_1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) topic contains additional information.</span></span>


```C++
#define PASSWORD L"new_password"

USER_INFO_1003 usriSetPassword;
//
// Set the usri1003_password member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriSetPassword.usri1003_password = PASSWORD;
    
netRet = NetUserSetInfo( SERVER, USERNAME, 1003, (LPBYTE)&usriSetPassword, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1003!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1003\n", netRet);
```



## <a name="setting-the-user-privilege-level-1005"></a><span data-ttu-id="80a8b-124">Configurando o privilégio de usuário, nível 1005</span><span class="sxs-lookup"><span data-stu-id="80a8b-124">Setting the User Privilege, Level 1005</span></span>

<span data-ttu-id="80a8b-125">O fragmento de código a seguir ilustra como especificar o nível de privilégio atribuído a um usuário com uma chamada para a função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="80a8b-125">The following code fragment illustrates how to specify the level of privilege assigned to a user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="80a8b-126">O [**tópico \_ informações \_ do usuário 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) contém informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="80a8b-126">The [**USER\_INFO\_1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) topic contains additional information.</span></span> <span data-ttu-id="80a8b-127">Para obter mais informações sobre privilégios de conta, consulte [constantes](/windows/desktop/SecAuthZ/authorization-constants)de [privilégios](/windows/desktop/SecAuthZ/privileges) e autorização.</span><span class="sxs-lookup"><span data-stu-id="80a8b-127">For more information about account privileges, see [Privileges](/windows/desktop/SecAuthZ/privileges) and [Authorization Constants](/windows/desktop/SecAuthZ/authorization-constants).</span></span>


```C++
USER_INFO_1005 usriPriv;
//
// Set the usri1005_priv member to the appropriate value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriPriv.usri1005_priv = USER_PRIV_USER;

netRet = NetUserSetInfo( SERVER, USERNAME, 1005, (LPBYTE)&usriPriv, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1005!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1005\n", netRet);
```



## <a name="setting-the-user-home-directory-level-1006"></a><span data-ttu-id="80a8b-128">Configurando o diretório base do usuário, nível 1006</span><span class="sxs-lookup"><span data-stu-id="80a8b-128">Setting the User Home Directory, Level 1006</span></span>

<span data-ttu-id="80a8b-129">O fragmento de código a seguir ilustra como especificar o caminho do diretório base de um usuário com uma chamada para a função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="80a8b-129">The following code fragment illustrates how to specify the path of a user's home directory with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="80a8b-130">O diretório pode ser um caminho embutido em código ou um caminho Unicode válido.</span><span class="sxs-lookup"><span data-stu-id="80a8b-130">The directory can be a hard-coded path or a valid Unicode path.</span></span> <span data-ttu-id="80a8b-131">O [**tópico \_ informações \_ do usuário 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) contém informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="80a8b-131">The [**USER\_INFO\_1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) topic contains additional information.</span></span>


```C++
#define HOMEDIR L"C:\\USER\USER_PATH"
USER_INFO_1006 usriHomeDir;
//
// Set the usri1006_home_dir member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriHomeDir.usri1006_home_dir = HOMEDIR;

netRet = NetUserSetInfo( SERVER, USERNAME, 1006, (LPBYTE)&usriHomeDir, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1006!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1006\n", netRet);
```



## <a name="setting-the-user-comment-field-level-1007"></a><span data-ttu-id="80a8b-132">Configurando o campo comentário do usuário, nível 1007</span><span class="sxs-lookup"><span data-stu-id="80a8b-132">Setting the User Comment Field, Level 1007</span></span>

<span data-ttu-id="80a8b-133">O fragmento de código a seguir ilustra como associar um comentário a um usuário chamando a função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="80a8b-133">The following code fragment illustrates how to associate a comment with a user by calling the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="80a8b-134">O [**tópico \_ informações \_ do usuário 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) contém informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="80a8b-134">The [**USER\_INFO\_1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) topic contains additional information.</span></span>


```C++
#define COMMENT L"This is my Comment Text for the user"
USER_INFO_1007 usriComment;
//
// Set the usri1007_comment member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriComment.usri1007_comment = COMMENT;

netRet = NetUserSetInfo( SERVER, USERNAME, 1007, (LPBYTE)&usriComment, NULL );

if( netRet == NERR_Success )
    printf("Success with level 1007!\n");
else
    printf( "ERROR: %d returned from NetUserSetInfo level 1007\n", netRet);
```



## <a name="setting-the-user-flags-level-1008"></a><span data-ttu-id="80a8b-135">Configurando os sinalizadores de usuário, nível 1008</span><span class="sxs-lookup"><span data-stu-id="80a8b-135">Setting the User Flags, Level 1008</span></span>

<span data-ttu-id="80a8b-136">O fragmento de código a seguir ilustra como definir sinalizadores de usuário com uma chamada para a função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="80a8b-136">The following code fragment illustrates how to set user flags with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="80a8b-137">O [**tópico \_ informações \_ do usuário 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) contém uma lista de valores válidos para os sinalizadores e uma descrição de cada sinalizador.</span><span class="sxs-lookup"><span data-stu-id="80a8b-137">The [**USER\_INFO\_1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) topic contains a list of valid values for the flags and a description of each flag.</span></span>

<span data-ttu-id="80a8b-138">Observe que o \_ sinalizador de script UF deve ser definido para redes Windows NT, windows 2000, Windows XP e LAN Manager.</span><span class="sxs-lookup"><span data-stu-id="80a8b-138">Note that the UF\_SCRIPT flag must be set for Windows NT, Windows 2000, Windows XP, and LAN Manager networks.</span></span> <span data-ttu-id="80a8b-139">A tentativa de definir outros sinalizadores sem configurar o \_ script UF nessas redes causará falha na função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="80a8b-139">Trying to set other flags without setting UF\_SCRIPT on these networks will cause the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function to fail.</span></span>


```C++
#define USR_FLAGS UF_SCRIPT | UF_NORMAL_ACCOUNT
USER_INFO_1008 usriFlags;
//
// Set the usri1008_flags member to the appropriate constant value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriFlags.usri1008_flags = USR_FLAGS;
netRet = NetUserSetInfo( SERVER, USERNAME, 1008, (LPBYTE)&usriFlags, NULL );
if( netRet == NERR_Success ) 
    printf("Success with level 1008!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1008\n", netRet);
```



## <a name="setting-the-user-script-path-level-1009"></a><span data-ttu-id="80a8b-140">Configurando o caminho do script do usuário, nível 1009</span><span class="sxs-lookup"><span data-stu-id="80a8b-140">Setting the User Script Path, Level 1009</span></span>

<span data-ttu-id="80a8b-141">O fragmento de código a seguir ilustra como definir o caminho para o arquivo de script de logon de um usuário específico com uma chamada para a função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="80a8b-141">The following code fragment illustrates how to set the path for the logon script file of a particular user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="80a8b-142">O arquivo de script pode ser um. Arquivo CMD, um. Arquivo EXE ou um. Arquivo BAT.</span><span class="sxs-lookup"><span data-stu-id="80a8b-142">The script file can be a .CMD file, an .EXE file, or a .BAT file.</span></span> <span data-ttu-id="80a8b-143">A cadeia de caracteres também pode ser nula.</span><span class="sxs-lookup"><span data-stu-id="80a8b-143">The string can also be null.</span></span> <span data-ttu-id="80a8b-144">O [**tópico \_ informações \_ do usuário 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) contém informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="80a8b-144">The [**USER\_INFO\_1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) topic contains additional information.</span></span>


```C++
#define SCRIPT_PATH L"C:\\BIN\\MYSCRIPT.BAT"
USER_INFO_1009 usriScrPath;
//
// Set the usri1009_script_path member to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriScrPath.usri1009_script_path = SCRIPT_PATH;
netRet = NetUserSetInfo( SERVER, USERNAME, 1009, (LPBYTE)&usriScrPath, NULL );
if( netRet == NERR_Success ) 
    printf("Success with level 1009!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1009\n", netRet);
```



## <a name="setting-the-user-authority-flags-level-1010"></a><span data-ttu-id="80a8b-145">Configurando os sinalizadores de autoridade de usuário, nível 1010</span><span class="sxs-lookup"><span data-stu-id="80a8b-145">Setting The User Authority Flags, Level 1010</span></span>

<span data-ttu-id="80a8b-146">O fragmento de código a seguir ilustra como definir os sinalizadores de privilégio de operador para um usuário com uma chamada para a função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="80a8b-146">The following code fragment illustrates how to set the operator privilege flags for a user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="80a8b-147">O [**tópico \_ informações \_ do usuário 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) contém uma lista de valores válidos para os sinalizadores e uma descrição de cada sinalizador.</span><span class="sxs-lookup"><span data-stu-id="80a8b-147">The [**USER\_INFO\_1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) topic contains a list of valid values for the flags and a description of each flag.</span></span>


```C++
#define AUTHORITY_FLAGS AF_OP_ACCOUNTS
USER_INFO_1010 usriAuthFlags;
//
// Set the usri1010_auth_flags member to the appropriate constant value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriAuthFlags.usri1010_auth_flags = AUTHORITY_FLAGS;
netRet = NetUserSetInfo( SERVER, USERNAME, 1010, (LPBYTE)&usriAuthFlags, NULL);
if( netRet == NERR_Success )
    printf("Success with level 1010!\n");
else
    printf( "ERROR: %d returned from NetUserSetInfo level 1010\n", netRet);
```



## <a name="setting-the-user-full-name-level-1011"></a><span data-ttu-id="80a8b-148">Definindo o nome completo do usuário, nível 1011</span><span class="sxs-lookup"><span data-stu-id="80a8b-148">Setting The User Full Name, Level 1011</span></span>

<span data-ttu-id="80a8b-149">O fragmento de código a seguir ilustra como definir o nome completo de um usuário com uma chamada para a função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="80a8b-149">The following code fragment illustrates how to set a user's full name with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="80a8b-150">O [**tópico \_ informações \_ do usuário 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) contém informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="80a8b-150">The [**USER\_INFO\_1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) topic contains additional information.</span></span>


```C++
#define USER_FULL_NAME L"Joe B. User"
USER_INFO_1011 usriFullName;
//
// Set the usri1011_full_name member to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriFullName.usri1011_full_name = USER_FULL_NAME;
netRet = NetUserSetInfo( SERVER, USERNAME, 1011, (LPBYTE)&usriFullName, NULL);
if( netRet == NERR_Success ) 
    printf("Success with level 1011!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo\n", netRet);
```



 

 
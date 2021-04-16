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
# <a name="changing-elements-of-user-information"></a>Alterando elementos de informações do usuário

As funções de gerenciamento de rede fornecem uma variedade de níveis de informações para ajudar a alterar as informações do usuário. Alguns níveis exigem privilégios administrativos para serem executados com êxito. Para obter mais informações sobre como chamar funções que exigem privilégios de administrador, consulte [executando com privilégios especiais](/windows/desktop/SecBP/running-with-special-privileges).

O código de exemplo neste tópico demonstra como alterar vários elementos de informações do usuário chamando a função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . O código usa várias estruturas de informações de gerenciamento de rede.

Ao alterar as informações do usuário, é melhor usar o nível específico para essa informação. Isso impede a redefinição acidental de informações não relacionadas ao usar os valores de nível inferior.

Definir alguns dos níveis mais comumente usados é ilustrado nos exemplos de código a seguir:

-   [Definindo a senha do usuário, nível 1003](#setting-the-user-password-level-1003)
-   [Configurando o privilégio de usuário, nível 1005](#setting-the-user-privilege-level-1005)
-   [Configurando o diretório base do usuário, nível 1006](#setting-the-user-home-directory-level-1006)
-   [Configurando o campo comentário do usuário, nível 1007](#setting-the-user-comment-field-level-1007)
-   [Configurando os sinalizadores de usuário, nível 1008](#setting-the-user-flags-level-1008)
-   [Configurando o caminho do script do usuário, nível 1009](#setting-the-user-script-path-level-1009)
-   [Configurando os sinalizadores de autoridade de usuário, nível 1010](#setting-the-user-authority-flags-level-1010)
-   [Definindo o nome completo do usuário, nível 1011](#setting-the-user-full-name-level-1011)

Todos os fragmentos de código pressupõem que o usuário definiu a diretiva de compilação UNICODE e incluiu os arquivos de cabeçalho do SDK apropriados, da seguinte maneira:


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



## <a name="setting-the-user-password-level-1003"></a>Definindo a senha do usuário, nível 1003

O fragmento de código a seguir ilustra como definir a senha de um usuário com um valor conhecido com uma chamada para a função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . O [**tópico \_ informações \_ do usuário 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) contém informações adicionais.


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



## <a name="setting-the-user-privilege-level-1005"></a>Configurando o privilégio de usuário, nível 1005

O fragmento de código a seguir ilustra como especificar o nível de privilégio atribuído a um usuário com uma chamada para a função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . O [**tópico \_ informações \_ do usuário 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) contém informações adicionais. Para obter mais informações sobre privilégios de conta, consulte [constantes](/windows/desktop/SecAuthZ/authorization-constants)de [privilégios](/windows/desktop/SecAuthZ/privileges) e autorização.


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



## <a name="setting-the-user-home-directory-level-1006"></a>Configurando o diretório base do usuário, nível 1006

O fragmento de código a seguir ilustra como especificar o caminho do diretório base de um usuário com uma chamada para a função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . O diretório pode ser um caminho embutido em código ou um caminho Unicode válido. O [**tópico \_ informações \_ do usuário 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) contém informações adicionais.


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



## <a name="setting-the-user-comment-field-level-1007"></a>Configurando o campo comentário do usuário, nível 1007

O fragmento de código a seguir ilustra como associar um comentário a um usuário chamando a função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . O [**tópico \_ informações \_ do usuário 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) contém informações adicionais.


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



## <a name="setting-the-user-flags-level-1008"></a>Configurando os sinalizadores de usuário, nível 1008

O fragmento de código a seguir ilustra como definir sinalizadores de usuário com uma chamada para a função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . O [**tópico \_ informações \_ do usuário 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) contém uma lista de valores válidos para os sinalizadores e uma descrição de cada sinalizador.

Observe que o \_ sinalizador de script UF deve ser definido para redes Windows NT, windows 2000, Windows XP e LAN Manager. A tentativa de definir outros sinalizadores sem configurar o \_ script UF nessas redes causará falha na função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .


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



## <a name="setting-the-user-script-path-level-1009"></a>Configurando o caminho do script do usuário, nível 1009

O fragmento de código a seguir ilustra como definir o caminho para o arquivo de script de logon de um usuário específico com uma chamada para a função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . O arquivo de script pode ser um. Arquivo CMD, um. Arquivo EXE ou um. Arquivo BAT. A cadeia de caracteres também pode ser nula. O [**tópico \_ informações \_ do usuário 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) contém informações adicionais.


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



## <a name="setting-the-user-authority-flags-level-1010"></a>Configurando os sinalizadores de autoridade de usuário, nível 1010

O fragmento de código a seguir ilustra como definir os sinalizadores de privilégio de operador para um usuário com uma chamada para a função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . O [**tópico \_ informações \_ do usuário 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) contém uma lista de valores válidos para os sinalizadores e uma descrição de cada sinalizador.


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



## <a name="setting-the-user-full-name-level-1011"></a>Definindo o nome completo do usuário, nível 1011

O fragmento de código a seguir ilustra como definir o nome completo de um usuário com uma chamada para a função [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) . O [**tópico \_ informações \_ do usuário 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) contém informações adicionais.


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



 

 
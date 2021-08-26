---
title: Códigos de erro LDAP para ADSI
description: Quando um servidor LDAP gera um erro e passa o erro para o cliente, o erro é então convertido em uma cadeia de caracteres pelo cliente LDAP.
ms.assetid: 7a0a5a1b-8473-405b-a590-3f917e50cbdc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b6280784d8bf9fc9c692cb38f1ca2d0e76646b1d2a3d464e516f03e7ac682fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005506"
---
# <a name="ldap-error-codes-for-adsi"></a>Códigos de erro LDAP para ADSI

Quando um servidor LDAP gera um erro e passa o erro para o cliente, o erro é então convertido em uma cadeia de caracteres pelo cliente LDAP.

Esse método é semelhante aos [códigos de erro do Win32 para ADSI](win32-error-codes-for-adsi.md). Neste exemplo, o código de erro do cliente é o erro 0x80072020 do WIN32.

**Para determinar os códigos de erro LDAP para ADSI**

1.  Descarte o 8007 do código de erro do WIN32. No exemplo, o valor hexadecimal restante é 2020.
2.  Converta o valor hexadecimal restante em um valor decimal. No exemplo, o valor hexadecimal restante 2020 converte para o valor decimal 8224.
3.  Pesquise no arquivo WinError. h para obter a definição do valor decimal. No exemplo, 8224L corresponde ao erro de erro **de \_ \_ operações DS \_**.
4.  Substitua o erro de prefixo **\_ DS** por **LDAP \_**. No exemplo, a nova definição é um **\_ \_ erro de operações LDAP**.
5.  Pesquise no arquivo Winldap. h o valor da definição de erro LDAP. No exemplo, o valor do **erro de \_ operações \_ LDAP** no arquivo Winldap. h é 0x01.

 

 





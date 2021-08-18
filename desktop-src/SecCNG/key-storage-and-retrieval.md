---
description: O CNG fornece um modelo para o armazenamento de chaves privadas que permite adaptar-se às demandas atuais e futuras de criação de aplicativos que usam recursos de criptografia, como criptografia de chave pública ou privada, bem como as demandas do armazenamento de material de chave.
ms.assetid: 95e5750f-fdc5-41f3-a4ce-9593a7081e95
title: Chave Armazenamento recuperação e recuperação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81b2100f005f0ff293e34a3f4c0a7460b7a4d4e9c2b15fbe0b3577b5e52394a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907677"
---
# <a name="key-storage-and-retrieval"></a>Chave Armazenamento recuperação e recuperação

-   [Arquitetura Armazenamento chave](#key-storage-architecture)
-   [Tipos de Chave](#key-types)
-   [Algoritmos com suporte](#supported-algorithms)
-   [Principais diretórios e arquivos](#key-directories-and-files)

## <a name="key-storage-architecture"></a>Arquitetura de Armazenamento chave

O CNG fornece um modelo para o armazenamento de chaves privadas que permite adaptar-se às demandas atuais e futuras de criação de aplicativos que usam recursos de criptografia, como criptografia de chave pública ou privada, bem como as demandas do armazenamento de material de chave. O roteador de armazenamento de chaves é a rotina central nesse modelo e é implementado em Ncrypt.dll. Um aplicativo acessa os KSPs (provedores de armazenamento de chaves) no sistema por meio do roteador de armazenamento de chaves, que oculta os detalhes, como o isolamento de chave, tanto do aplicativo quanto do próprio provedor de armazenamento. A ilustração a seguir mostra o design e a função da arquitetura de isolamento de chave CNG.

![provedor de armazenamento de chaves cng](images/cng-key-storage-provider.png)

Para atender aos requisitos de CC (critérios comuns), as chaves de longa duração devem ser isoladas para que elas nunca sejam presentes no processo do aplicativo. Atualmente, o CNG dá suporte ao armazenamento de chaves privadas assimétricas usando o KSP de software da Microsoft incluído no Windows Server 2008 e Windows Vista e instalado por padrão.

O isolamento de chave é habilitado por padrão Windows Server 2008 e Windows Vista. O recurso de isolamento de chave não está disponível em plataformas anteriores a elas. Além disso, KSPs de terceiros não são carregados no serviço de isolamento de chave (processo LSA). Somente o Microsoft KSP é carregado no serviço de isolamento de chave.

O processo LSA é usado como o processo de isolamento de chave para maximizar o desempenho. Todo o acesso a chaves privadas passa pelo roteador de armazenamento de chaves, que expõe um conjunto abrangente de funções para gerenciar e usar chaves privadas.

O CNG armazena a parte pública da chave armazenada separadamente da parte privada. A parte pública de um par de chaves também é mantida no serviço de isolamento de chave e é acessada usando lRPC (chamada de procedimento remoto local). O roteador de armazenamento de chaves usa LRPC ao chamar o processo de isolamento de chave. Todo o acesso a chaves privadas passa pelo roteador de chave privada e é auditado pelo CNG.

Conforme descrito acima, há suporte para uma ampla variedade de dispositivos de armazenamento de hardware. Em cada caso, a interface para todos esses dispositivos de armazenamento é idêntica. Ele inclui funções para executar várias operações de chave privada, bem como funções que pertencem ao armazenamento e ao gerenciamento de chaves.

O CNG fornece um conjunto de APIs que são usadas para criar, armazenar e recuperar chaves criptográficas. Para ver uma lista dessas APIs, consulte [CNG Key Armazenamento Functions](cng-key-storage-functions.md).

## <a name="key-types"></a>Tipos de Chave

O CNG dá suporte aos seguintes tipos de chave:

-   Diffie-Hellman chaves públicas e privadas.
-   Chaves públicas e privadas do algoritmo de assinatura digital (DSA, FIPS 186-2).
-   Chaves públicas e privadas rsa (PKCS \# 1).
-   Várias chaves públicas e privadas herdadas (CryptoAPI).
-   Chaves públicas e privadas da Criptografia de Curva Elíptica.

## <a name="supported-algorithms"></a>Algoritmos com suporte

O CNG dá suporte aos seguintes algoritmos de chave.

| Algoritmo | Comprimento da chave/hash (bits)             |
|-----------|------------------------------------|
| RSA       | 512 a 16384, em incrementos de 64 bits |
| Dh        | 512 a 16384, em incrementos de 64 bits |
| DSA       | 512 a 1024, em incrementos de 64 bits  |
| ECDSA     | P-256, P-384, P-521 (curvas NIST)  |
| ECDH      | P-256, P-384, P-521 (curvas NIST)  |
| MD2       | 128                                |
| MD4       | 128                                |
| MD5       | 128                                |
| SHA-1     | 160                                |
| SHA-256   | 256                                |
| SHA-384   | 384                                |
| SHA-512   | 512                                |



 

## <a name="key-directories-and-files"></a>Principais diretórios e arquivos

Os CSPs de CryptoAPI herdados da Microsoft armazenam chaves privadas nos diretórios a seguir.

| Tipo de chave                | Diretórios                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Privado do usuário            | %APPDATA% \\ SID de Usuário do Microsoft Crypto \\ \\ RSA \\ \\<br/>%APPDATA% SID de \\ usuário do Microsoft Crypto \\ \\ DSS \\ \\<br/>                                                   |
| Sistema local privado    | %ALLUSERSPROFILE% \\ dados do aplicativo Microsoft Crypto RSA \\ \\ \\ \\ S-1-5-18\\<br/>%ALLUSERSPROFILE% \\ dados do aplicativo Microsoft Crypto \\ \\ \\ DSS \\ S-1-5-18\\<br/>   |
| Serviço local privado   | %ALLUSERSPROFILE% \\ dados do aplicativo Microsoft Crypto RSA \\ \\ \\ \\ S-1-5-19\\<br/>%ALLUSERSPROFILE% \\ dados do aplicativo Microsoft Crypto \\ \\ \\ DSS \\ S-1-5-19\\<br/>   |
| Serviço de rede privado | %ALLUSERSPROFILE% \\ dados do aplicativo Microsoft Crypto RSA \\ \\ \\ \\ S-1-5-20\\<br/>%ALLUSERSPROFILE% \\ dados do aplicativo Microsoft Crypto \\ \\ \\ DSS \\ S-1-5-20\\<br/>   |
| Privado compartilhado          | %ALLUSERSPROFILE% \\ dados do aplicativo Microsoft Crypto RSA \\ \\ \\ \\ MachineKeys<br/>%ALLUSERSPROFILE% \\ dados do aplicativo Microsoft Crypto \\ \\ \\ DSS \\ MachineKeys<br/> |



 

O CNG armazena chaves privadas nos diretórios a seguir.

| Tipo de chave                | Diretório                                                          |
|-------------------------|--------------------------------------------------------------------|
| Privado do usuário            | %APPDATA% \\ Chaves de Criptografia da Microsoft \\ \\                                 |
| Sistema local privado    | %ALLUSERSPROFILE% \\ dados do aplicativo Microsoft Crypto \\ \\ \\ SystemKeys |
| Serviço local privado   | %WINDIR% \\ ServiceProfiles \\ LocalService                            |
| Serviço de rede privado | %WINDIR% \\ ServiceProfiles \\ NetworkService                          |
| Privado compartilhado          | %ALLUSERSPROFILE% \\ dados do aplicativo Microsoft Crypto \\ \\ \\ Keys       |



 

A seguir estão algumas das diferenças entre os contêineres de chave CryptoAPI e CNG.

-   O CNG usa nomes de arquivo diferentes para arquivos de chave que os arquivos de chave criados pelo Rsaenh.dll e Dssenh.dll CSPs herdados. Os arquivos de chave herdados também têm a extensão .key, mas os arquivos de chave CNG não têm a extensão .key.
-   A CNG dá suporte total a nomes de contêiner de chave Unicode; A CNG usa um hash do nome do contêiner Unicode, enquanto o CryptoAPI usa um hash do nome do contêiner ANSI.
-   A CNG é mais flexível em relação aos pares de chaves RSA. Por exemplo, a CNG dá suporte a expoentes públicos maiores que 32 bits de comprimento e oferece suporte a chaves nas quais p e q são tamanhos diferentes.
-   No CryptoAPI, o arquivo de contêiner de chave é armazenado em um diretório cujo nome é o equivalente textual do SID do usuário. Esse não é mais o caso na CNG, o que elimina a dificuldade de mover usuários de um domínio para outro sem perder todas as suas chaves privadas.
-   O KSP de CNG e os nomes de chave são limitados a caracteres Unicode de **\_ caminho máximo** . O CSP e os nomes de chave do CryptoAPI são limitados aos caracteres ANSI **máximos do \_ caminho** .
-   A CNG oferece a capacidade de propriedades de chave definidas pelo usuário. Os usuários podem criar e associar Propriedades personalizadas a chaves e tê-las armazenadas com chaves persistentes.

Ao persistir uma chave, a CNG pode criar dois arquivos. O primeiro arquivo contém a chave privada no novo formato CNG e é sempre criado. Esse arquivo não pode ser usado pelos CSPs do CryptoAPI herdados. O segundo arquivo contém a mesma chave privada no contêiner de chave CryptoAPI herdada. O segundo arquivo está em conformidade com o formato e o local usados pelo Rsaenh.dll. A criação do segundo arquivo só ocorrerá se o sinalizador **NCRYPT \_ Write \_ Key \_ para o \_ \_ repositório \_ herdado** for especificado quando a função [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) for chamada para finalizar uma chave RSA. Não há suporte para esse recurso em chaves DSA e DH.

Quando um aplicativo tenta abrir uma chave persistente existente, a CNG tenta primeiro abrir o arquivo CNG nativo. Se esse arquivo não existir, a CNG tentará localizar uma chave correspondente no contêiner de chave CryptoAPI herdado.

quando você move ou copia chaves de CryptoAPI de um computador de origem para um computador de destino com Ferramenta de Migração do Usuário Windows (USMT), a CNG falhará ao acessar as chaves no computador de destino. Para acessar essas chaves migradas, você deve usar o CryptoAPI.

 

 





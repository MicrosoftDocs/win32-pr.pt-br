---
description: A CNG fornece um modelo de armazenamento de chave privada que permite adaptar às demandas atuais e futuras da criação de aplicativos que usam recursos de criptografia, como criptografia de chave privada ou pública, bem como as demandas do armazenamento de material da chave.
ms.assetid: 95e5750f-fdc5-41f3-a4ce-9593a7081e95
title: Armazenamento e recuperação de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5abfd6319353440c580d53990075a71613a1eba9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297200"
---
# <a name="key-storage-and-retrieval"></a>Armazenamento e recuperação de chave

-   [Arquitetura de armazenamento de chaves](#key-storage-architecture)
-   [Tipos de Chave](#key-types)
-   [Algoritmos com suporte](#supported-algorithms)
-   [Diretórios-chave e arquivos](#key-directories-and-files)

## <a name="key-storage-architecture"></a>Arquitetura de armazenamento de chaves

A CNG fornece um modelo de armazenamento de chave privada que permite adaptar às demandas atuais e futuras da criação de aplicativos que usam recursos de criptografia, como criptografia de chave privada ou pública, bem como as demandas do armazenamento de material da chave. O roteador de armazenamento de chaves é a rotina central nesse modelo e é implementado em Ncrypt.dll. Um aplicativo acessa os KSPs (provedores de armazenamento de chaves) no sistema por meio do roteador de armazenamento de chaves, que oculta os detalhes, como o isolamento de chave, do aplicativo e do próprio provedor de armazenamento. A ilustração a seguir mostra o design e a função da arquitetura de isolamento de chave CNG.

![provedor de armazenamento de chaves CNG](images/cng-key-storage-provider.png)

Para atender aos requisitos de protocolo CC, as chaves de vida longa devem ser isoladas para que nunca estejam presentes no processo do aplicativo. Atualmente, a CNG dá suporte ao armazenamento de chaves privadas assimétricas usando o KSP de software da Microsoft que está incluído no Windows Server 2008 e no Windows Vista e instalado por padrão.

O isolamento de chave é habilitado por padrão no Windows Server 2008 e no Windows Vista. O recurso de isolamento de chave não está disponível em plataformas antes delas. Além disso, KSPs de terceiros não são carregados no serviço de isolamento de chaves (processo LSA). Somente o KSP da Microsoft é carregado no serviço de isolamento de chave.

O processo LSA é usado como o processo de isolamento de chave para maximizar o desempenho. Todo o acesso a chaves privadas passa pelo roteador de armazenamento de chaves, que expõe um conjunto abrangente de funções para gerenciar e usar chaves privadas.

A CNG armazena a parte pública da chave armazenada separadamente da parte privada. A parte pública de um par de chaves também é mantida no serviço de isolamento de chave e é acessada usando o LRPC (chamada de procedimento remoto) local. O roteador de armazenamento de chaves usa o LRPC ao chamar o processo de isolamento de chave. Todo o acesso a chaves privadas passa pelo roteador de chave privada e é auditado pela CNG.

Conforme descrito acima, é possível oferecer suporte a uma grande variedade de dispositivos de armazenamento de hardware. Em cada caso, a interface para todos esses dispositivos de armazenamento é idêntica. Ele inclui funções para executar várias operações de chave privada, bem como funções que pertencem ao armazenamento e gerenciamento de chaves.

A CNG fornece um conjunto de APIs que são usadas para criar, armazenar e recuperar chaves criptográficas. Para obter uma lista dessas APIs, consulte [funções de armazenamento de chave CNG](cng-key-storage-functions.md).

## <a name="key-types"></a>Tipos de Chave

A CNG dá suporte aos seguintes tipos de chave:

-   Diffie-Hellman chaves públicas e privadas.
-   Algoritmo de assinatura digital (DSA, FIPS 186-2) chaves públicas e privadas.
-   \#Chaves públicas e privadas RSA (PKCS 1).
-   Várias chaves públicas e privadas herdadas (CryptoAPI).
-   Chaves públicas e privadas da criptografia de curva elíptica.

## <a name="supported-algorithms"></a>Algoritmos com suporte

A CNG dá suporte aos seguintes algoritmos de chave.

| Algoritmo | Comprimento de chave/hash (bits)             |
|-----------|------------------------------------|
| RSA       | 512 a 16384, em incrementos de bits 64 |
| FEITA        | 512 a 16384, em incrementos de bits 64 |
| DSA       | 512 a 1024, em incrementos de bits 64  |
| ECDSA     | P-256, P-384, P-521 (curvas NIST)  |
| ECDH      | P-256, P-384, P-521 (curvas NIST)  |
| MD2       | 128                                |
| MD4       | 128                                |
| MD5       | 128                                |
| SHA-1     | 160                                |
| SHA-256   | 256                                |
| SHA-384   | 384                                |
| SHA-512   | 512                                |



 

## <a name="key-directories-and-files"></a>Diretórios-chave e arquivos

Os CSPs do CryptoAPI herdados da Microsoft armazenam chaves privadas nos diretórios a seguir.

| Tipo de chave                | Diretórios                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Usuário privado            | % APPDATA% \\ Sid de usuário do Microsoft \\ crypto \\ RSA \\ \\<br/>% APPDATA% \\ Sid de usuário do Microsoft \\ crypto \\ DSS \\ \\<br/>                                                   |
| Particular do sistema local    | % ALLUSERSPROFILE% de \\ dados de aplicativos \\ Microsoft \\ crypto \\ RSA \\ S-1-5-18\\<br/>% ALLUSERSPROFILE% de \\ dados \\ de aplicativos Microsoft \\ crypto \\ DSS \\ S-1-5-18\\<br/>   |
| Serviço local particular   | % ALLUSERSPROFILE% de \\ dados de aplicativos \\ Microsoft \\ crypto \\ RSA \\ S-1-5-19\\<br/>% ALLUSERSPROFILE% de \\ dados \\ de aplicativos Microsoft \\ crypto \\ DSS \\ S-1-5-19\\<br/>   |
| Serviço de rede particular | % ALLUSERSPROFILE% de \\ dados de aplicativos \\ Microsoft \\ crypto \\ RSA \\ S-1-5-20\\<br/>% ALLUSERSPROFILE% de \\ dados \\ de aplicativos Microsoft \\ crypto \\ DSS \\ S-1-5-20\\<br/>   |
| Privado compartilhado          | % ALLUSERSPROFILE% de \\ dados de aplicativos \\ Microsoft \\ crypto \\ RSA \\ MachineKeys<br/>% ALLUSERSPROFILE% de \\ dados de aplicativos \\ Microsoft \\ crypto \\ DSS \\ MachineKeys<br/> |



 

A CNG armazena chaves privadas nos diretórios a seguir.

| Tipo de chave                | Diretório                                                          |
|-------------------------|--------------------------------------------------------------------|
| Usuário privado            | % APPDATA% \\ \\ chaves de criptografia da Microsoft \\                                 |
| Particular do sistema local    | % ALLUSERSPROFILE% de \\ dados de aplicativos \\ Microsoft \\ crypto \\ SystemKeys |
| Serviço local particular   | % WINDIR% \\ Improfiles \\ LocalService                            |
| Serviço de rede particular | % WINDIR% \\ UserProfiles \\ NetworkService                          |
| Privado compartilhado          | % ALLUSERSPROFILE% de \\ dados de aplicativo chaves de criptografia da \\ Microsoft \\ \\       |



 

A seguir estão algumas das diferenças entre os contêineres de chave CryptoAPI e CNG.

-   A CNG usa nomes de arquivo diferentes para arquivos de chave do que arquivos de chave que são criados pelo Rsaenh.dll e Dssenh.dll CSPs herdados. Os arquivos de chave herdados também têm a extensão. Key, mas os arquivos de chave CNG não têm a extensão. Key.
-   A CNG dá suporte total a nomes de contêiner de chave Unicode; A CNG usa um hash do nome do contêiner Unicode, enquanto o CryptoAPI usa um hash do nome do contêiner ANSI.
-   A CNG é mais flexível em relação aos pares de chaves RSA. Por exemplo, a CNG dá suporte a expoentes públicos maiores que 32 bits de comprimento e oferece suporte a chaves nas quais p e q são tamanhos diferentes.
-   No CryptoAPI, o arquivo de contêiner de chave é armazenado em um diretório cujo nome é o equivalente textual do SID do usuário. Esse não é mais o caso na CNG, o que elimina a dificuldade de mover usuários de um domínio para outro sem perder todas as suas chaves privadas.
-   O KSP de CNG e os nomes de chave são limitados a caracteres Unicode de **\_ caminho máximo** . O CSP e os nomes de chave do CryptoAPI são limitados aos caracteres ANSI **máximos do \_ caminho** .
-   A CNG oferece a capacidade de propriedades de chave definidas pelo usuário. Os usuários podem criar e associar Propriedades personalizadas a chaves e tê-las armazenadas com chaves persistentes.

Ao persistir uma chave, a CNG pode criar dois arquivos. O primeiro arquivo contém a chave privada no novo formato CNG e é sempre criado. Esse arquivo não pode ser usado pelos CSPs do CryptoAPI herdados. O segundo arquivo contém a mesma chave privada no contêiner de chave CryptoAPI herdada. O segundo arquivo está em conformidade com o formato e o local usados pelo Rsaenh.dll. A criação do segundo arquivo só ocorrerá se o sinalizador **NCRYPT \_ Write \_ Key \_ para o \_ \_ repositório \_ herdado** for especificado quando a função [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) for chamada para finalizar uma chave RSA. Não há suporte para esse recurso em chaves DSA e DH.

Quando um aplicativo tenta abrir uma chave persistente existente, a CNG tenta primeiro abrir o arquivo CNG nativo. Se esse arquivo não existir, a CNG tentará localizar uma chave correspondente no contêiner de chave CryptoAPI herdado.

Quando você move ou copia chaves de CryptoAPI de um computador de origem para um computador de destino com Ferramenta de Migração do Usuário Windows (USMT), a CNG falhará ao acessar as chaves no computador de destino. Para acessar essas chaves migradas, você deve usar o CryptoAPI.

 

 





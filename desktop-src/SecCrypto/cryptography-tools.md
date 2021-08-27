---
description: As ferramentas de criptografia fornecem ferramentas de linha de comando para assinatura de código, verificação de assinatura e outras tarefas de criptografia.
ms.assetid: 21adbcfb-fadd-4818-9dc5-23bfd526b525
title: Ferramentas de criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9547ba1d3a13958859c2f0504c60a1a1bbe4a67403c9709bb57900b73ad3a50d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100976"
---
# <a name="cryptography-tools"></a>Ferramentas de criptografia

As ferramentas de criptografia fornecem ferramentas de linha de comando para assinatura de código, verificação de assinatura e outras tarefas de criptografia.

## <a name="introduction-to-code-signing"></a>Introdução à assinatura de código

O setor de software deve fornecer aos usuários os meios para confiar no código, incluindo o código publicado na Internet. Muitas páginas da Web contêm apenas informações estáticas que podem ser baixadas com pouco risco. No entanto, algumas páginas contêm controles e aplicativos a serem baixados e executados no computador de um usuário. Esses arquivos executáveis podem ser arriscados de serem baixados e executados.

O software empacotado usa marcas e saídas de vendas confiáveis para garantir a integridade dos usuários, mas essas garantias não estão disponíveis quando o código é transmitido pela Internet. Além disso, a Própria Internet não pode fornecer nenhuma garantia sobre a identidade do criador de software. Também não pode garantir que qualquer software baixado não foi alterado após sua criação. Os navegadores podem exibir uma mensagem de aviso que explica os possíveis riscos de baixar dados de qualquer tipo, mas os navegadores não podem verificar se o código é o que ele declara ser. Uma abordagem mais ativa deve ser usada para tornar a Internet uma mídia confiável para distribuição de software.

Uma abordagem para fornecer garantias de autenticidade [*e*](../secgloss/i-gly.md) integridade dos arquivos é anexar [*assinaturas digitais*](../secgloss/d-gly.md) a esses arquivos. Uma assinatura digital anexada a um arquivo identifica positivamente o distribuidor desse arquivo e garante que o conteúdo do arquivo não foi alterado depois que a assinatura foi criada.

Assinaturas digitais podem ser criadas e verificadas usando as APIs de criptografia da Microsoft. Para obter informações básicas sobre criptografia e [*as funções CryptoAPI,*](../secgloss/c-gly.md) consulte [Cryptography Essentials](cryptography-essentials.md).

Para obter informações [*detalhadas sobre assinaturas*](../secgloss/d-gly.md)digitais, [*certificados*](../secgloss/c-gly.md)e [*armazenamentos de certificados,*](../secgloss/c-gly.md)consulte os seguintes tópicos:

-   [Hashes e assinaturas digitais](hashes-and-digital-signatures.md)
-   [Certificados Digitais](digital-certificates.md)
-   [Gerenciando certificados com armazenamentos de certificados](managing-certificates-with-certificate-stores.md)
-   [Verificação de confiança de certificado](certificate-trust-verification.md)

Atualmente, as Ferramentas cryptoAPI são compatíveis com a tecnologia Microsoft Authenticode, permitindo que os fornecedores de software assinem os seguintes tipos de arquivos para verificação do Authenticode.



| Extensão de nome de arquivo                             | Sumário                                                                                                                                                                                                                              |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .appx<br/>                                | Arquivos do instalador para um Windows de dispositivo da Windows Store.<br/>                                                                                                                                                                            |
| .cab<br/>                                 | Arquivos autossu contidos usados para instalação e instalação de aplicativos. Em um arquivo de gabinete, vários arquivos são compactados em um arquivo. Normalmente, eles são encontrados em discos de distribuição de software da Microsoft.<br/>                        |
| .cat<br/>                                 | Arquivos que contêm [*impressões digitais*](../secgloss/t-gly.md) de vários arquivos. Um arquivo .cat pode ser usado para garantir a integridade dos arquivos cujas impressões digitais ele inclui.<br/> |
| .dll<br/>                                 | Arquivos que contêm funções executáveis.<br/>                                                                                                                                                                                   |
| .exe<br/>                                 | Arquivos que contêm programas executáveis.<br/>                                                                                                                                                                                    |
| .js<br/> .vbs<br/> .wsf<br/>  | Windows arquivos shell para JScript ou Microsoft Visual Basic VBScript (Scripting Edition).<br/>                                                                                                                                    |
| .msi<br/> .msp<br/> .mst<br/> | Windows do instalador.<br/>                                                                                                                                                                                                   |
| .ocx<br/>                                 | Arquivos que contêm controles ActiveX Microsoft.<br/>                                                                                                                                                                             |
| .ps1<br/>                                 | Arquivos que contêm scripts do PowerShell.<br/>                                                                                                                                                                                     |
| .stl<br/>                                 | Arquivos que contêm uma CTL [*(lista de*](../secgloss/c-gly.md) confiança de certificado).<br/>                                                                           |
| .sys<br/>                                 | Arquivos que contêm binários de driver.<br/>                                                                                                                                                                                        |



 

Para obter informações sobre assinatura digital, consulte os seguintes documentos:

-   CCITT, Recomendação X.509, *The Directory-Authentication Framework*, Comitê de Consultoria, Telefone Internacional eIa, International Telecommunications Union, Geneva, 1989.
-   RSA Rsa Rsa, *PKCS \# 7: Padrão de* sintaxe de mensagem de criptografia. Versão 1.5, novembro de 1993.
-   Schneier, Ltda, *Applied Cryptography*, 2d ed. Nova York: John & Sons, 1996.
-   [https://www.rsa.com](https://www.rsa.com/)

> [!Note]  
> Esses recursos podem não estar disponíveis em alguns idiomas e países ou regiões.

 

## <a name="microsoft-cryptography-tools"></a>Ferramentas de Criptografia da Microsoft

As ferramentas de publicação e a DLL de assinatura são instaladas no \\ diretório Bin da instalação do SDK da Microsoft. Eles incluem os arquivos a seguir.



| Nome do arquivo                    | Comentários                                                                                                                                                                                             |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cert2SPC.exe](cert2spc.md) | Cria um [*SPC (Certificado Publisher software)*](../secgloss/s-gly.md) somente para fins de teste.<br/> |
| [CertMgr.exe](certmgr.md)   | Gerencia certificados, CTLs e CRLs (listas [*de*](../secgloss/c-gly.md) certificados revogados).<br/>             |
| [MakeCat.exe](makecat.md)   | Cria um arquivo de catálogo não assinado que contém os hashes de um conjunto de arquivos juntamente com atributos associados de cada arquivo.<br/>                                                               |
| [MakeCert.exe](makecert.md) | Cria um [*certificado X.509 apenas*](../secgloss/x-gly.md) para fins de teste.<br/>                                                                      |
| Pvk2pfx.exe                  | Converte um arquivo de certificado do publicador de software (.spc) ou um arquivo de chave privada (.pvk Exchange) em formato de arquivo PFX (Informações Pessoais).<br/>                                                   |
| [SetReg.exe](setreg.md)     | Define as chaves do Registro que controlam a verificação do certificado.<br/>                                                                                                                                |
| [SignTool.exe](signtool.md) | Assina e marca um arquivo. Além disso, verifica a assinatura de um arquivo.<br/>                                                                                                              |



 

 

 

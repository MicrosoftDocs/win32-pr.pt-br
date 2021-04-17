---
description: As ferramentas de criptografia fornecem ferramentas de linha de comando para assinatura de código, verificação de assinatura e outras tarefas de criptografia.
ms.assetid: 21adbcfb-fadd-4818-9dc5-23bfd526b525
title: Ferramentas de criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8003bb002bd8d203547779c96bc15491a5418169
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770350"
---
# <a name="cryptography-tools"></a>Ferramentas de criptografia

As ferramentas de criptografia fornecem ferramentas de linha de comando para assinatura de código, verificação de assinatura e outras tarefas de criptografia.

## <a name="introduction-to-code-signing"></a>Introdução à assinatura de código

O setor de software deve fornecer aos usuários meios para confiar no código, incluindo o código publicado na Internet. Muitas páginas da Web contêm apenas informações estáticas que podem ser baixadas com pouco risco. Algumas páginas, no entanto, contêm controles e aplicativos a serem baixados e executados no computador de um usuário. Esses arquivos executáveis podem ser arriscados para serem baixados e executados.

O software empacotado usa a identidade visual e as vendas confiáveis para garantir os usuários de sua integridade, mas essas garantias não estão disponíveis quando o código é transmitido na Internet. Além disso, a própria Internet não pode fornecer nenhuma garantia sobre a identidade do criador de software. Nem pode garantir que nenhum software baixado não tenha sido alterado após sua criação. Os navegadores podem exibir uma mensagem de aviso que explica os possíveis perigos de baixar dados de qualquer tipo, mas os navegadores não podem verificar se o código é o que alega ser. Uma abordagem mais ativa deve ser tomada para tornar a Internet uma mídia confiável para a distribuição de software.

Uma abordagem para fornecer garantias da autenticidade e da [*integridade*](../secgloss/i-gly.md) dos arquivos é anexar [*assinaturas digitais*](../secgloss/d-gly.md) a esses arquivos. Uma assinatura digital anexada a um arquivo identifica positivamente o distribuidor desse arquivo e garante que o conteúdo do arquivo não tenha sido alterado após a criação da assinatura.

As assinaturas digitais podem ser criadas e verificadas usando as APIs de criptografia da Microsoft. Para obter informações básicas sobre criptografia e as funções de [*CryptoAPI*](../secgloss/c-gly.md) , consulte [princípios básicos de criptografia](cryptography-essentials.md).

Para obter informações detalhadas sobre [*assinaturas digitais*](../secgloss/d-gly.md), [*certificados*](../secgloss/c-gly.md)e [*repositórios de certificados*](../secgloss/c-gly.md), consulte os seguintes tópicos:

-   [Hashes e assinaturas digitais](hashes-and-digital-signatures.md)
-   [Certificados digitais](digital-certificates.md)
-   [Gerenciando certificados com repositórios de certificados](managing-certificates-with-certificate-stores.md)
-   [Verificação de confiança de certificado](certificate-trust-verification.md)

Atualmente, as ferramentas de CryptoAPI dão suporte à tecnologia Microsoft Authenticode, permitindo que os fornecedores de software assinem os seguintes tipos de arquivos para verificação de Authenticode.



| Extensão de nome de arquivo                             | Sumário                                                                                                                                                                                                                              |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .appx<br/>                                | Arquivos do instalador para um aplicativo de dispositivo da Windows Store.<br/>                                                                                                                                                                            |
| .cab<br/>                                 | Arquivos independentes usados para instalação e instalação de aplicativos. Em um arquivo de gabinete, vários arquivos são compactados em um arquivo. Normalmente, eles são encontrados em discos de distribuição de software da Microsoft.<br/>                        |
| .cat<br/>                                 | Arquivos que contêm [*impressões*](../secgloss/t-gly.md) digitais de vários arquivos. Um arquivo. Cat pode ser usado para garantir a integridade dos arquivos cujas impressões digitais ela inclui.<br/> |
| .dll<br/>                                 | Arquivos que contêm funções executáveis.<br/>                                                                                                                                                                                   |
| .exe<br/>                                 | Arquivos que contêm programas executáveis.<br/>                                                                                                                                                                                    |
| .js<br/> .vbs<br/> .wsf<br/>  | Arquivos de shell do Windows para JScript ou Microsoft Visual Basic Scripting Edition (VBScript).<br/>                                                                                                                                    |
| .msi<br/> .msp<br/> .mst<br/> | Arquivos do Windows Installer.<br/>                                                                                                                                                                                                   |
| .ocx<br/>                                 | Arquivos que contêm controles ActiveX da Microsoft.<br/>                                                                                                                                                                             |
| .ps1<br/>                                 | Arquivos que contêm scripts do PowerShell.<br/>                                                                                                                                                                                     |
| . STL<br/>                                 | Arquivos que contêm uma CTL ( [*lista de certificados confiáveis*](../secgloss/c-gly.md) ).<br/>                                                                           |
| .sys<br/>                                 | Arquivos que contêm binários de driver.<br/>                                                                                                                                                                                        |



 

Para obter informações sobre a assinatura digital, consulte os seguintes documentos:

-   CCITT, Recomendação X. 509, *estrutura de Directory-Authentication*, Comitê de consultoria, telefone internacional e Telegraph, União Internacional de telecomunicações, Geneva, 1989.
-   RSA Laboratories, *PKCS \# 7: padrão de sintaxe de mensagem de criptografia*. Versão 1,5, novembro de 1993.
-   Schneier, Bruce, *criptografia aplicada*, 2D Ed. Nova York: John Wiley & filhos, 1996.
-   [https://www.rsa.com](https://www.rsa.com/)

> [!Note]  
> Esses recursos podem não estar disponíveis em alguns idiomas e países ou regiões.

 

## <a name="microsoft-cryptography-tools"></a>Ferramentas de criptografia da Microsoft

As ferramentas de publicação e a DLL de assinatura são instaladas no \\ diretório bin da instalação do Microsoft SDK. Eles incluem os arquivos a seguir.



| Nome do arquivo                    | Comentários                                                                                                                                                                                             |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cert2SPC.exe](cert2spc.md) | Cria um [*certificado do fornecedor de software*](../secgloss/s-gly.md) (SPC) somente para fins de teste.<br/> |
| [CertMgr.exe](certmgr.md)   | Gerencia certificados, CTLs e listas de certificados [*revogados*](../secgloss/c-gly.md) (CRLs).<br/>             |
| [MakeCat.exe](makecat.md)   | Cria um arquivo de catálogo não assinado que contém os hashes de um conjunto de arquivos junto com os atributos associados de cada arquivo.<br/>                                                               |
| [MakeCert.exe](makecert.md) | Cria um certificado [*X. 509*](../secgloss/x-gly.md) apenas para fins de teste.<br/>                                                                      |
| Pvk2pfx.exe                  | Converte um arquivo de certificado do fornecedor de software (. SPC) ou um arquivo de chave privada (. pvk) para o formato de arquivo PFX (troca de informações pessoais).<br/>                                                   |
| [SetReg.exe](setreg.md)     | Define as chaves do registro que controlam a verificação de certificado.<br/>                                                                                                                                |
| [SignTool.exe](signtool.md) | Sinal e carimbo de data/hora de um arquivo. Além disso, o verifica a assinatura de um arquivo.<br/>                                                                                                              |



 

 

 

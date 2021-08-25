---
description: Use tecnologias criptográficas para criptografia de chave pública, algoritmos de criptografia, criptografia RSA e certificados digitais.
ms.assetid: c53af815-ee3f-417a-8e62-3a3689715bc6
title: Criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050f84d118cb5ad9e1da49ddabd73489745339bb0b1357e229b0f1609a1c997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876106"
---
# <a name="cryptography"></a>Criptografia

## <a name="purpose"></a>Finalidade

Criptografia é o uso de códigos para converter dados para que apenas um destinatário específico possa lê-los usando uma chave.

As tecnologias criptográficas da Microsoft incluem CryptoAPI, CSP (Cryptographic Service Providers), CryptoAPI Tools, CAPICOM, WinTrust, emissão e gerenciamento de certificados e desenvolvimento de infraestruturas de chave pública personalizáveis. Registro de certificado e cartão inteligente, gerenciamento de certificados e desenvolvimento de módulo personalizado também são descritos.

## <a name="developer-audience"></a>Público de desenvolvedores

CryptoAPI destina-se ao uso por desenvolvedores de aplicativos baseados em Windows que permitirão que os usuários criem e troquem documentos e outros dados em um ambiente seguro, especialmente em mídias não seguras, como a Internet. Os desenvolvedores devem estar familiarizados com as linguagens de programação C e C++ e o Windows de programação. Embora não seja necessário, é aconselhável compreender a criptografia ou os assuntos relacionados à segurança.

CAPICOM é um componente somente de 32 bits que se destina ao uso por desenvolvedores que estão criando aplicativos usando a linguagem de programação Visual Basic VBScript (Scripting Edition) ou a linguagem de programação C++. CAPICOM está disponível para uso nos sistemas operacionais especificados em Run-Time Requisitos. Para desenvolvimento futuro, recomendamos que você use o .NET Framework para implementar recursos de segurança. Para obter mais informações, [consulte Alternativas ao uso de CAPICOM.](alternatives-to-using-capicom.md)

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Para obter informações sobre os requisitos de tempo de executar para um elemento de programação específico, consulte a seção Requisitos da página de referência para esse elemento.

O CAPICOM 2.1.0.2 tem suporte nos seguintes sistemas operacionais e versões:

-   Windows Server 2003
-   Windows XP

CAPICOM está disponível como um arquivo redistribuível que pode ser baixado do [SDK da Plataforma Redistribuível: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281).

Os Serviços de Certificados exigem as seguintes versões desses sistemas operacionais:

-   Windows Server 2008 R2
-   Windows Server 2008
-   Windows Server 2003

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                           | Descrição                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre a criptografia](about-cryptography.md)<br/>         | Principais conceitos de criptografia e uma exibição de alto nível das tecnologias de criptografia da Microsoft.<br/>                                                                                                                           |
| [Usando criptografia](using-cryptography.md)<br/>         | Processos de criptografia, procedimentos e exemplos estendidos de programas C e Visual Basic usando funções CryptoAPI e objetos CAPICOM.<br/>                                                                            |
| [Referência de criptografia](cryptography-reference.md)<br/> | Descrições detalhadas das funções de criptografia da Microsoft, interfaces, objetos, estruturas e outros elementos de programação da Microsoft. Inclui descrições de referência da API para trabalhar com certificados digitais.<br/> |



 

 

 





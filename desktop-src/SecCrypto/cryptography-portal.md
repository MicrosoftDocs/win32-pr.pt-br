---
description: Use tecnologias de criptografia para criptografia de chave pública, algoritmos de criptografia, criptografia RSA e certificados digitais.
ms.assetid: c53af815-ee3f-417a-8e62-3a3689715bc6
title: Criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852b7c2b38ca5b7d330a70e91a5b7a9dd5bb6557
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811286"
---
# <a name="cryptography"></a>Criptografia

## <a name="purpose"></a>Finalidade

Criptografia é o uso de códigos para converter dados para que apenas um destinatário específico possa lê-los, usando uma chave.

As tecnologias de criptografia da Microsoft incluem CryptoAPI, CSP (provedores de serviços de criptografia), ferramentas de CryptoAPI, CAPICOM, a emissão e o gerenciamento de certificados e o desenvolvimento de infraestruturas de chave pública personalizáveis. O registro de certificado e de cartão inteligente, o gerenciamento de certificados e o desenvolvimento de módulos personalizados também são descritos.

## <a name="developer-audience"></a>Público de desenvolvedores

O CryptoAPI destina-se a ser usado por desenvolvedores de aplicativos baseados no Windows que permitirão que os usuários criem e troquem documentos e outros dados em um ambiente seguro, especialmente em mídias não seguras, como a Internet. Os desenvolvedores devem estar familiarizados com as linguagens de programação C e C++ e o ambiente de programação do Windows. Embora não seja necessário, uma compreensão de criptografia ou de assuntos relacionados à segurança é aconselhada.

O capicor é um componente somente de 32 bits que se destina ao uso por desenvolvedores que estão criando aplicativos usando a linguagem de programação Visual Basic Scripting Edition (VBScript) ou a linguagem de programação C++. O CAPICOM está disponível para uso nos sistemas operacionais especificados nos requisitos de Run-Time. Para desenvolvimento futuro, recomendamos que você use o .NET Framework para implementar recursos de segurança. Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da página de referência para esse elemento.

CAPICOM 2.1.0.2 tem suporte nos seguintes sistemas operacionais e versões:

-   Windows Server 2003
-   Windows XP

O CAPICOM está disponível como um arquivo redistribuível que pode ser baixado de [Platform SDK Redistributable: CApicom](https://www.microsoft.com/download/details.aspx?id=25281).

Os serviços de certificados requerem as seguintes versões desses sistemas operacionais:

-   Windows Server 2008 R2
-   Windows Server 2008
-   Windows Server 2003

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                           | Descrição                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre criptografia](about-cryptography.md)<br/>         | Conceitos de criptografia de chave e uma exibição de alto nível das tecnologias de criptografia da Microsoft.<br/>                                                                                                                           |
| [Usando criptografia](using-cryptography.md)<br/>         | Processos de criptografia, procedimentos e amostras estendidas de programas C e Visual Basic usando funções CryptoAPI e objetos CAPICOM.<br/>                                                                            |
| [Referência de criptografia](cryptography-reference.md)<br/> | Descrições detalhadas das funções de criptografia, interfaces, objetos, estruturas e outros elementos de programação da Microsoft. Inclui descrições de referência da API para trabalhar com certificados digitais.<br/> |



 

 

 





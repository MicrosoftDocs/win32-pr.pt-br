---
description: O XML é um padrão do setor para descrever dados estruturados. Uma assinatura digital XML é uma representação XML de uma assinatura digital que fornece a capacidade de verificar a origem e a integridade do documento XML e de dados referenciados externamente.
ms.assetid: 02ca8d9b-be08-4b15-895f-9c8c4b0ed536
title: Visão geral da assinatura digital XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41a1b748305ab26b686e126cd201ad9e7f34d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811046"
---
# <a name="xml-digital-signature-overview"></a>Visão geral da assinatura digital XML

O XML é um padrão do setor para descrever dados estruturados. Uma assinatura digital XML é uma representação XML de uma [*assinatura digital*](../secgloss/d-gly.md) que fornece a capacidade de verificar a origem e a integridade do documento XML e de dados referenciados externamente. As assinaturas digitais XML podem ser usadas para assinar dados arbitrários, incluindo um documento ou fragmento XML, uma página HTML, texto sem formatação ou dados codificados em binários, como um arquivo JPEG.

O formato de assinatura digital XML com suporte da API de assinatura digital CryptXML é especificado pela recomendação W3C de sintaxe e processamento (segunda edição) de assinatura XML.

A assinatura digital CryptXML implementa o suporte para os tipos de assinatura necessários, algoritmos criptográficos, algoritmos de canonização e a transformação envelopada especificada.

Os desenvolvedores podem estender o conjunto padrão de algoritmos criptográficos com suporte do CryptXML criando DLLs de extensão criptográfica. Os desenvolvedores também podem criar suas próprias transformações personalizadas e algoritmos de canonização na parte superior da API do CryptXML. Os desenvolvedores podem usar as APIs do CryptXML com as APIs de certificado do Windows.

 

 

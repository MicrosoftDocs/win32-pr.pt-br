---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1680f8fe426c2e3a62cac0674928a1520b402357
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105756687"
---
# <a name="cert2spc"></a>Cert2SPC

A ferramenta Cert2SPC cria um certificado de teste do [*fornecedor de software*](../secgloss/s-gly.md) (SPC) usando [*certificados*](../secgloss/c-gly.md) [*X. 509*](../secgloss/x-gly.md) existentes. Cert2SPC pode encapsular vários certificados X. 509 em um objeto de dados assinado [*PKCS \# 7*](../secgloss/p-gly.md) . A ferramenta é instalada na \\ pasta bin do caminho de instalação do SDK (Software Development Kit) do Microsoft Windows.

O Cert2SPC está disponível como parte do SDK do Windows, do qual você pode baixar <https://go.microsoft.com/fwlink/p/?linkid=84091> .

> [!Note]
> Essa ferramenta é apenas para fins de teste. Um SPC válido é obtido de uma [*autoridade de certificação*](../secgloss/c-gly.md).


**Cert2SPC** *Cert1. cer Cert2. cer* ... *Output. SPC*

 



|                         |                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| *Cert1. cer Cert2. cer* ... | Nomes dos certificados X. 509 a serem incluídos no SPC. Cada nome de certificado termina com a extensão. cer.                         |
| *Output. SPC*            | Nome do objeto PKCS \# 7 que contém os certificados X. 509 a serem criados. O nome do arquivo de saída termina com a extensão. SPC. |



 

 

 

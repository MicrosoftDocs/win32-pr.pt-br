---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66405ffb881e9ab384037bf9e388d3e055c4186a322efe0ab4171da4ece605e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127226"
---
# <a name="cert2spc"></a>Cert2SPC

a ferramenta Cert2SPC cria um certificado de teste de [*Publisher de Software*](../secgloss/s-gly.md) (SPC) usando [*certificados*](../secgloss/c-gly.md) [*X. 509*](../secgloss/x-gly.md) existentes. Cert2SPC pode encapsular vários certificados X. 509 em um objeto de dados assinado [*PKCS \# 7*](../secgloss/p-gly.md) . a ferramenta é instalada na \\ pasta Bin do caminho de instalação do Software Development Kit (SDK) do Microsoft Windows.

o Cert2SPC está disponível como parte do SDK do Windows, do qual você pode baixar <https://go.microsoft.com/fwlink/p/?linkid=84091> .

> [!Note]
> Essa ferramenta é apenas para fins de teste. Um SPC válido é obtido de uma [*autoridade de certificação*](../secgloss/c-gly.md).


**Cert2SPC** *Cert1. cer Cert2. cer* ... *Output. SPC*

 



| Parâmetros              | Descrição                                                                                                                        |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| *Cert1. cer Cert2. cer* ... | Nomes dos certificados X. 509 a serem incluídos no SPC. Cada nome de certificado termina com a extensão. cer.                         |
| *Output. SPC*            | Nome do objeto PKCS \# 7 que contém os certificados X. 509 a serem criados. O nome do arquivo de saída termina com a extensão. SPC. |



 

 

 

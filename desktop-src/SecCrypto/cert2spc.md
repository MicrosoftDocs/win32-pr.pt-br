---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 419f0e6dc6f1183252f138029dadc7817ac3b5ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581974"
---
# <a name="cert2spc"></a>Cert2SPC

A ferramenta Cert2SPC cria um SPC [*(Certificado*](../secgloss/s-gly.md) Publisher software) de teste usando certificados [*X.509*](../secgloss/x-gly.md) [*existentes.*](../secgloss/c-gly.md) Cert2SPC pode envolver vários certificados X.509 em um objeto de dados assinados [*PKCS \# 7.*](../secgloss/p-gly.md) A ferramenta é instalada na pasta Bin do caminho de instalação do \\ SDK (Software Development Kit) do Microsoft Windows.

O Cert2SPC está disponível como parte do SDK do Windows, que você pode baixar do <https://go.microsoft.com/fwlink/p/?linkid=84091> .

> [!Note]
> Essa ferramenta é apenas para fins de teste. Um SPC válido é obtido de uma autoridade de [*certificação*](../secgloss/c-gly.md).


**Cert2SPC** *Cert1.cer Cert2.cer...* *Output.spc*

 



| Parâmetros              | Descrição                                                                                                                        |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| *Cert1.cer Cert2.cer...* | Nomes dos certificados X.509 a incluir no SPC. Cada nome de certificado termina com a extensão .cer.                         |
| *Output.spc*            | Nome do objeto PKCS \# 7 que contém os certificados X.509 a serem criados. O nome do arquivo de saída termina com a extensão .spc. |



 

 

 

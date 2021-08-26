---
description: Pktextract.exe é uma ferramenta que extrai o atributo publicKeyToken de um arquivo de certificado.
ms.assetid: 195ff5bd-bb60-4053-9308-ceacd29853c0
title: Pktextract.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7f2cbb210262a05839ac3a7df71f3bedea603a5ea959249867efc2d5e420e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884947"
---
# <a name="pktextractexe"></a>Pktextract.exe

Pktextract.exe é uma ferramenta que extrai o atributo **PublicKeyToken** de um arquivo de certificado. A saída é o **PublicKeyToken**, que é um identificador exclusivo de 16 caracteres (8 bytes) da chave pública presente no certificado, em um formato que pode ser facilmente colado em uma instrução de identidade do assembly. O arquivo de certificado deve estar presente no mesmo diretório que Pktextract.exe para usar o utilitário. Pktextract.exe é fornecido no SDK (Software Development Kit) do Microsoft Windows.

## <a name="syntax"></a>Syntax

**pktextract.exe** *<filename. cer>* **\[ -Quiet \] \[ -nologo \]**

## <a name="command-line-options"></a>Opções de linha de comando

Pktextract.exe usa as seguintes opções de linha de comando que não diferenciam maiúsculas de minúsculas.



| Opção  | Descrição                                                          |
|---------|----------------------------------------------------------------------|
| -quiet  | Suprime a exibição completa de informações de certificado. Opcional.        |
| -nologo | É executado sem exibir dados padrão de direitos autorais da Microsoft. Opcional. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ferramentas de desenvolvimento lado a lado do assembly](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 




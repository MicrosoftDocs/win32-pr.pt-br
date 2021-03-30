---
title: Entrada de registro de tempo de execução
description: Entrada de registro de tempo de execução
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Windows Media Player, entradas de registro de tempo de execução
- Windows Media Player, extensões de nome de arquivo
- Windows Media Player, registro
- registro, extensões de nome de arquivo
- registro, entradas de tempo de execução
- registro, configurações do Windows Media Player
- configurações do registro de extensão de nome de arquivo
- entradas do registro em tempo de execução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01a83c3642f49a9fdbe7f8c51f157a154a9843b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005763"
---
# <a name="runtime-registry-entry"></a>Entrada de registro de tempo de execução

Quando o Windows Media Player encontra uma extensão de nome de arquivo Personalizada, ele procura uma subchave do registro que corresponda à extensão. A subchave é descrita em [configurações de registro de extensão de nome de arquivo](file-name-extension-registry-settings.md). Uma das entradas do registro que podem aparecer na subchave da extensão é a entrada de **tempo de execução** .

A entrada de **tempo de execução** especifica a tecnologia subjacente que o Windows Media Player pode usar para reproduzir ou converter arquivos de mídia digital que têm a extensão personalizada. A entrada de **tempo de execução** tem o seguinte formato.



|          |                |                                                               |
|----------|----------------|---------------------------------------------------------------|
| **Nome** | **Tipo**       | **Valor**                                                     |
| Runtime  | **REG \_ DWORD** | Um inteiro positivo que identifica a tecnologia subjacente. |



 

O valor da entrada de **tempo de execução** deve ser um dos seguintes.



| **Valor (Decimal)** | **Descrição**                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| 6                   | Renderizar usando o Windows Media Format SDK.                                                 |
| 7                   | Renderizar usando o Microsoft DirectShow.                                                         |
| 13                  | Converta o arquivo usando o plug-in de conversão especificado. Requer o Windows Media Player 11. |



 

Os valores de entrada do registro de **tempo de execução** 6 e 7 têm suporte do Windows Media Player 9 Series e posterior. O valor 13 é suportado pelo Windows Media Player 11.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Subchave ConvertPluginCLSID**](convertpluginclsid-subkey.md)
</dt> <dt>

[**Configurações do registro de extensão de nome de arquivo**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 





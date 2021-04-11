---
title: Entrada do registro FormatCode
description: Entrada do registro FormatCode
ms.assetid: cc444eaa-6898-48ab-9573-9e7d5e25d6db
keywords:
- Windows Media Player, entradas do registro FormatCode
- Windows Media Player, extensões de nome de arquivo
- Windows Media Player, registro
- registro, extensões de nome de arquivo
- registro, entradas FormatCode
- registro, configurações do Windows Media Player
- configurações do registro de extensão de nome de arquivo
- Entradas do registro FormatCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2318d32e9d7a08a2ae23b24e7acd2674b9eecb2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104161789"
---
# <a name="formatcode-registry-entry"></a>Entrada do registro FormatCode

Quando o Windows Media Player encontra uma extensão de nome de arquivo Personalizada, ele procura uma subchave do registro que corresponda à extensão. A subchave é descrita em [configurações de registro de extensão de nome de arquivo](file-name-extension-registry-settings.md). Uma das entradas do registro que podem aparecer sob a subchave da extensão é a entrada **FormatCode** .

A entrada de registro **FormatCode** especifica o código de formato do MTP (protocolo de transporte de mídia) para arquivos que têm a extensão personalizada. A entrada do registro **FormatCode** tem o seguinte formato.



| Nome       | Tipo           | Valor                                                             |
|------------|----------------|-------------------------------------------------------------------|
| FormatCode | **REG \_ DWORD** | Um inteiro positivo de 16 bits que identifica o formato do arquivo. |



 

Quando o usuário tenta copiar um arquivo de mídia digital que tem uma extensão de nome de arquivo Personalizada para um dispositivo portátil, o Windows Media Player examina o registro para localizar um código de formato associado à extensão de nome de arquivo personalizado. Se o Windows Media Player encontrar um código de formato, ele usará MTP para determinar se o dispositivo dá suporte ao formato de arquivo personalizado. Se o dispositivo der suporte ao formato, o arquivo de mídia será copiado para o dispositivo sem ser transcodificado.

Um dispositivo que dá suporte a MTP pode fornecer ao Windows Media Player um conjunto de DeviceInfo, que contém, entre outras coisas, uma lista de códigos de formato com suporte pelo dispositivo.

Se você estiver no processo de desenvolvimento de um formato de arquivo personalizado, poderá solicitar um código de formato da Microsoft. Para obter informações sobre como solicitar um código de formato, consulte o Microsoft Media Transport Protocol Porting Kit, que está disponível no [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurações do registro de extensão de nome de arquivo**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 





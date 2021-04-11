---
description: Comandos
ms.assetid: f579745a-5327-4c8b-bfa7-fe81d9657a3b
title: Comandos (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974c6b2b68949e53ae778ed56adcfcb10d2edd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164419"
---
# <a name="commands-wpd-api"></a>Comandos (API WPD)

O aplicativo cliente e o driver se comunicam por meio de comandos que são enviados do cliente (por meio da API de dispositivo portátil do Windows) para o driver (por meio da estrutura de driver do User-Mode). Um comando pode ou não incluir um parâmetro e pode ou não retornar um resultado. Um cliente pode enviar um comando explicitamente, chamando o método [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) ou o método **IPortableDeviceService: SendCommand** , ou implicitamente, chamando qualquer um dos métodos das interfaces de cliente. Alguns comandos só podem ser enviados explicitamente; Eles são indicados na documentação do comando. As páginas de referência de comando descrevem a finalidade de um comando, bem como os parâmetros que espera receber e quais parâmetros devem ser retornados.

Um comando é identificado por uma estrutura **PROPERTYKEY** . Isso é composto de duas partes: uma parte de GUID (o membro *fmtid* ) e uma parte DWORD (o membro *pid* ). A parte GUID é usada para indicar a categoria à qual o comando pertence (comandos relacionados pertencem à mesma categoria e, portanto, terão o mesmo *fmtid*). A parte DWORD indica a ID de comando e é usada para distinguir os comandos individuais dentro de uma categoria de comando (os valores de *pid* para comandos na mesma categoria serão diferentes).

A tabela a seguir lista as categorias de comandos que os dispositivos portáteis do Windows definem. Os fabricantes de dispositivos podem definir seus próprios comandos criando suas próprias categorias de comando e IDs de comando. No entanto, um fabricante não deve adicionar comandos às categorias listadas abaixo, pois elas são reservadas pela Microsoft.

**Categorias de comando**



| Categoria de comando                         | Descrição                                                                                                                             |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Categoria de WPD \_ \_ comum**                | Comandos que são comuns a todos os objetos e dispositivos.                                                                                    |
| **\_dicas de \_ dispositivo de categoria WPD \_**         | Comandos que são usados para recuperar informações opcionais do dispositivo que podem ser usadas para melhorar a experiência do usuário final.                         |
| **Categoria de WPD do \_ \_ SMS**                   | Comandos que são usados para dispositivos que oferecem suporte à funcionalidade SMS, que normalmente é exposta em telefones celulares. |
| **a \_ categoria \_ WPD \_ ainda \_ captura de imagem** | Comandos que são usados para dispositivos que dão suporte à captura de imagem ainda.                                                                    |
| **\_armazenamento de categoria WPD \_**               | Comandos que são usados para objetos funcionais de armazenamento.                                                                                  |



 

Os comandos específicos definidos para cada um desses tipos são fornecidos nas tabelas a seguir, organizadas por tipo de comando.

**Categoria \_ comum da categoria WPD \_**



| Comando                                                                                | Descrição        |
|----------------------------------------------------------------------------------------|--------------------|
| [**\_comando de \_ \_ redefinição comum de comandos WPD \_**](wpd-command-common-reset-device-command.md) | Redefine o dispositivo. |



 

**Categoria \_ de \_ dicas de dispositivo de categoria WPD \_**



| Comando                                                                                                              | Descrição                                                                      |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**\_dicas de dispositivo de comando WPD \_ \_ \_ obter \_ local do conteúdo \_**](wpd-command-device-hints-get-content-location-command.md) | Recupera as IDs de objeto das pastas que podem conter um objeto de um tipo especificado. |



 

**Categoria de armazenamento de \_ categoria WPD \_**



| Comando                                                                     | Descrição                                                         |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**\_ejeção de \_ armazenamento de comando WPD \_**](wpd-command-storage-eject-command.md)   | Ejeta um meio de armazenamento que pode ser ejetado remotamente pelo driver. |
| [**\_formato de \_ armazenamento de comando WPD \_**](wpd-command-storage-format-command.md) | Formata um objeto funcional de armazenamento no dispositivo.                  |



 

**Categoria da \_ categoria de SMS de WPD \_**



| Comando                                                         | Descrição                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| [**\_comando de \_ envio de SMS para o WPD \_**](wpd-command-sms-send-command.md) | Inicia o envio de uma mensagem SMS por um objeto funcional do SMS. |



 

**Categoria de WPD de \_ \_ \_ imagem ainda categoria \_**



| Comando                                                                                                   | Descrição                                                         |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**comando WPD- \_ \_ captura de \_ imagem ainda \_ \_ iniciada**](wpd-command-still-image-capture-initiate-command.md) | Inicia uma captura de imagem ainda por um objeto funcional de imagem ainda. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 




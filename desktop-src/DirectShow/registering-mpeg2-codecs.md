---
description: Registrando codecs MPEG2
ms.assetid: f730a7df-af8f-4dce-9bfe-6ee1eca8fd90
title: Registrando codecs MPEG2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de007cebdd0a911f6b43f21003ed3ede0bc1723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087477"
---
# <a name="registering-mpeg2-codecs"></a>Registrando codecs MPEG2

Este tópico aplica-se somente ao Windows XP Media Center Edition.

O Windows XP Media Center Edition mantém duas chaves do registro que ele usa para determinar qual codec usar para reproduzir arquivos de vídeo e áudio do MPEG2. A primeira chave do Registro especifica o codec MPEG2 preferencial do fabricante do computador e a segunda lista todos os codecs compatíveis com o Media Center que estão atualmente instalados no computador. Quando o Media Center precisar reproduzir um arquivo MPEG2, ele usará o codec preferencial do fabricante, se um for especificado. Caso contrário, ele usará o primeiro codec compatível com o Media Center listado no registro. Se o registro não especificar nenhum codec preferencial ou compatível, o Media Center usará o mérito de filtro padrão do DirectShow para escolher um codec.

Para garantir que o Media Center sempre use um codec MPEG2 compatível, os fabricantes de computadores do Media Center devem especificar o codec do MPEG2 preferencial no seguinte local do registro:


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Media Center\Service\Video
```



Os dados de chave devem ser os seguintes:


```C++
PreferredMPEG2VideoDecoder=REG_SZ "{MPEG2 Video CLSID GUID}"
PreferredMPEG2AudioDecoder=REG_SZ "{MPEG2 Audio CLSID GUID}"
```



O programa de instalação para um codec MPEG2 compatível com o Media Center deve registrar o codec criando duas instâncias da seguinte chave do registro — uma para o codec de vídeo e outra para o codec de áudio:


```C++
[HKEY_CLASSES_ROOT\CLSID\{083863F1-70DE-11d0-BD40-00A0C911CE86}\Instance\<Your Codec CLSID here>\Capabilities]
```



Os dados de chave devem ser os seguintes:


```C++
"{374ac4df-7c98-4257-b13d-36087dbee458}"=dword:00000001
```



 

 




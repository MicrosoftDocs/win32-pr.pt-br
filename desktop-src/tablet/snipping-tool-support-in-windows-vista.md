---
description: Este tópico descreve como seu aplicativo pode especificar qual URL a ferramenta de recorte do Tablet PC deve obter ao capturar seu aplicativo.
ms.assetid: e31e63e8-8f6b-41f7-8bd6-afc5ca32456b
title: Suporte a ferramentas de recorte no Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046dd6c8a97d1dacc20065dc1f741610fec13865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829377"
---
# <a name="snipping-tool-support-in-windows-vista"></a>Suporte a ferramentas de recorte no Windows Vista

Este tópico descreve como seu aplicativo pode especificar qual URL a ferramenta de recorte do Tablet PC deve obter ao capturar seu aplicativo.

## <a name="specifying-the-url-via-registry-key"></a>Especificando a URL por meio da chave do registro

A ferramenta de recorte permite que os usuários capturem um recorte (captura de tela) de qualquer objeto na tela e, em seguida, anotem, salvem ou compartilhem a imagem. Quando os dados são salvos em formato HTML, ou quando são enviados a um cliente de email que dá suporte a HTML embutido, a ferramenta de recorte pode adicionar uma URL ao recorte se o aplicativo fornecer informações sobre como obter a URL.

A ferramenta de recorte Obtém a URL por meio de objetos de acessibilidade. Os aplicativos devem especificar as informações necessárias nas seguintes chaves do registro:

HKLM \\ software \\ Microsoft \\ Windows \\ Tablet \\ \\ reLinkFingerprintstion Tool,

E deve criar uma subchave cujo nome seja o mesmo da classe de janela da qual o link deve ser obtido. O nome da classe da janela deve ser a janela mais alta do aplicativo.

HKLM \\ software \\ Microsoft \\ Windows \\ Tablet \\ \\ LinkFingerprints Tool\\<Window Class Name>

### <a name="window-class-key-details"></a>Detalhes da chave da classe Window

Na chave de classe da janela, os valores apropriados devem ser definidos para indicar que a ferramenta de recorte deve detectar o objeto de acessibilidade correto.



| VALOR                        | TYPE                  | MASCARA            | INFORMAÇÕES ARMAZENADAS                                          |
|------------------------------|-----------------------|-----------------|-------------------------------------------------------------|
| Mask<br/>              | REG \_ DWORD<br/> |                 | Indica quais dos campos a seguir verificar<br/> |
| Name<br/>              | REG \_ sz<br/>    | 0x02<br/> | Nome de acessibilidade<br/>                               |
| Description<br/>       | REG \_ sz<br/>    | 0x04<br/> | Descrição da acessibilidade<br/>                        |
| Função<br/>              | REG \_ DWORD<br/> | 0x08<br/> | Função de acessibilidade<br/>                               |
| ParentName<br/>        | REG \_ sz<br/>    | 0x10<br/> | Nome de acessibilidade do pai<br/>                     |
| Paivalue<br/>       | REG \_ sz<br/>    | 0x20<br/> | Valor de acessibilidade do pai<br/>                    |
| ParentRole<br/>        | REG \_ DWORD<br/> | 0x40<br/> | Função de acessibilidade do pai<br/>                     |
| ParentDescription<br/> | REG \_ sz<br/>    | 0x80<br/> | Descrição de acessibilidade do pai<br/>              |



 

Além disso, se o valor de bit de máscara 0x1 for definido, a URL deverá ser extraída do nome de acessibilidade; caso contrário, a URL deve ser retirada do valor de acessibilidade.

Se o aplicativo usar cadeias de caracteres localizadas para os valores de REG \_ sz acima, a cadeia de caracteres deverá ser fornecida como uma cadeia indireta usando o seguinte formato:

@filename, recurso

A cadeia de caracteres é extraída do arquivo chamado, usando o valor do recurso como um localizador. Se o valor do recurso for zero ou maior, o número se tornará o índice da cadeia de caracteres no arquivo binário. Se o número for negativo, ele se tornará um identificador de recurso (ID).

> [!Note]  
> As constantes de função podem ser encontradas em OleAcc. h na SDK do Windows. Os valores de registro descritos são específicos do Windows Vista.

 

 

 





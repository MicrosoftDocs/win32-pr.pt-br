---
title: Espaço de Configuração do Dispositivo
description: O espaço de configuração de um dispositivo é o conjunto de todos os valores possíveis que podem ser atribuídos a todos os atributos do dispositivo.
ms.assetid: 598299c3-159f-4cad-b6a5-d282cd5bb4a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e09eabf7c84e1990e0aaf6b2d9fab1d9043f788fef32c3863a71d9ca1e6b61a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092106"
---
# <a name="device-configuration-space-and-device-configurations"></a>Espaço de Configuração do Dispositivo e Configurações do Dispositivo

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O espaço de *configuração de um* dispositivo é o conjunto de todos os valores possíveis que podem ser atribuídos a todos os atributos do dispositivo. Os dois motivos mais importantes para descrever o espaço de configuração do dispositivo em PrintCapabilities são os seguintes.

1.  As informações contribuem significativamente para uma maior compreensão dos recursos do dispositivo. Essas informações facilitam para um cliente do PrintCapabilities gerar elementos de interface do usuário, o que facilita para o usuário final selecionar uma configuração específica para processar um trabalho. Ao fornecer mais detalhes sobre os recursos do dispositivo para o aplicativo e, por fim, para o usuário final, a intenção de impressão do usuário pode ser atendida com mais eficiência.

2.  Determinadas propriedades de dispositivo apresentadas no PrintCapabilities podem depender da configuração específica selecionada pelo cliente.

Algumas informações não devem ser incorporadas em PrintCapabilities. Isso inclui informações que não afetam a maneira como um trabalho é criado, não impõe restrições na maneira como um trabalho é criado, nem afeta as propriedades do dispositivo. Por exemplo, um dispositivo pode ser capaz de relatar informações de status, como o conjunto de trabalhos aguardando para serem processados. Essas informações não têm efeito sobre as informações necessárias para formatar o trabalho, nem fornecem nenhuma indicação dos recursos disponíveis no dispositivo. Por esse motivo, esse tipo de informação não precisa estar presente em PrintCapabilities.

## <a name="device-constraints"></a>Restrições de dispositivo

Muitos dispositivos não são compatíveis com todas as configurações possíveis no espaço de configuração devido a uma restrição no dispositivo. Por exemplo, um dispositivo pode ser restringido da execução de impressão duplex em mídia transparente. Uma restrição pode representar uma limitação física: alguns tipos de mídia são simplesmente rígidos demais para percorrer determinados caminhos de papel no dispositivo e, portanto, não podem ser colocados em alguns slots de entrada ou roteados para alguns compartimentos de saída. Atualmente, é responsabilidade do provedor PrintCapabilities ou PrintTicket validar a configuração representada pela entrada PrintTicket, para verificar se ela não representa uma configuração inválida. Se a configuração for inválida, o provedor PrintCapabilities ou PrintTicket deverá modificar a configuração de forma que ela se torne válida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




---
title: Espaço de configuração do dispositivo
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 598299c3-159f-4cad-b6a5-d282cd5bb4a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120e12b6480675dba6e735390f4820a8782edc5c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105761241"
---
# <a name="device-configuration-space-and-device-configurations"></a>Espaço de configuração do dispositivo e configurações do dispositivo

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O espaço de *configuração* de um dispositivo é o conjunto de todos os valores possíveis que podem ser atribuídos a todos os atributos do dispositivo. Os dois motivos mais importantes para descrever o espaço de configuração do dispositivo nos recursos de PrintCapabilities são os seguintes.

1.  As informações contribuem significativamente para uma compreensão maior dos recursos do dispositivo. Essas informações tornam mais fácil para um cliente das PrintCapabilities gerar elementos da interface do usuário, o que torna mais fácil para o usuário final selecionar uma configuração específica para processar um trabalho. Ao fornecer mais detalhes sobre os recursos do dispositivo para o aplicativo e, finalmente, para o usuário final, a intenção de impressão do usuário pode ser cumprida com mais eficiência.

2.  Determinadas propriedades de dispositivo apresentadas nos PrintCapabilities podem ser dependentes da configuração específica selecionada pelo cliente.

Algumas informações não devem ser incorporadas a PrintCapabilities. Isso inclui informações que não afetam a maneira como um trabalho é criado, não impõe restrições na maneira como um trabalho é criado, nem afeta as propriedades do dispositivo. Por exemplo, um dispositivo pode ser capaz de relatar informações de status, como o conjunto de trabalhos aguardando para serem processados. Essas informações não têm nenhum efeito sobre as informações necessárias para formatar o trabalho, nem fornece nenhuma indicação dos recursos disponíveis no dispositivo. Por esse motivo, esse tipo de informação não precisa estar presente nos PrintCapabilities.

## <a name="device-constraints"></a>Restrições de dispositivo

Muitos dispositivos não dão suporte a todas as configurações possíveis no espaço de configuração devido a uma restrição no dispositivo. Por exemplo, um dispositivo pode ser restrito da execução de impressão duplex em mídia transparente. Uma restrição pode representar uma limitação física: alguns tipos de mídia são simplesmente muito rígidos para percorrer determinados caminhos de papel no dispositivo e, portanto, não podem ser colocados em alguns slots de entrada ou ser roteados para alguns compartimentos de saída. Atualmente, é responsabilidade do fornecedor de PrintCapabilities ou PrintTicket validar a configuração representada pelo PrintTicket de entrada, para verificar se ela não representa uma configuração inválida. Se a configuração for inválida, o provedor de PrintCapabilities ou PrintTicket deverá modificar a configuração de forma que ela se torne válida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




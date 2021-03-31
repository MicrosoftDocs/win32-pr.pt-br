---
title: Propriedade SRStatus
description: Propriedade SRStatus
ms.assetid: 67618a35-05e4-4bb3-b910-c75de6e32578
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64cb6ba16bc024a52b65efa98c22fd089ad79da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006186"
---
# <a name="srstatus-property"></a>Propriedade SRStatus

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna se a entrada de fala pode ser iniciada para o caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agente. ***Caracteres ("*** characterid * * *"). SRStatus**



| Valor | Descrição                                                                                                                                                                                                                               |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | As condições dão suporte à entrada de fala.                                                                                                                                                                                                          |
| 1     | Não há nenhum dispositivo de entrada de áudio disponível neste sistema. (Observe que isso não detecta se um microfone está instalado; ele só pode detectar se o usuário tem uma placa de som habilitada para entrada devidamente instalada com um driver funcional.) |
| 2     | Outro cliente é o cliente ativo desse caractere ou o caractere atual não é o mais alto.                                                                                                                                           |
| 3     | O canal de entrada ou saída de áudio está ocupado no momento, um aplicativo está usando áudio.                                                                                                                                                       |
| 4     | Ocorreu um erro não especificado no processo de inicialização do subsistema de reconhecimento de fala. Isso inclui a possibilidade de que não haja um mecanismo de fala disponível correspondente à configuração de idioma do caractere.                          |
| 5     | O usuário desabilitou a entrada de fala nas opções de caractere avançado.                                                                                                                                                                     |
| 6     | Ocorreu um erro ao verificar o status de áudio, mas a causa do erro não foi retornada pelo sistema.                                                                                                                                |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa propriedade retorna as condições necessárias para dar suporte à entrada de fala, incluindo o status do dispositivo de áudio. Você pode verificar essa propriedade antes de chamar o método [**Listen**](listen-method.md) para garantir melhor seu sucesso.

Quando a entrada de fala está habilitada na folha de propriedades do agente (opções avançadas de caractere), a consulta dessa propriedade carregará o mecanismo associado, se ele ainda não estiver carregado, e iniciará os serviços de fala. Ou seja, a chave de escuta está disponível e a dica de escuta é automaticamente displayável. (A chave de escuta e a dica de escuta serão habilitadas somente se elas também estiverem habilitadas em opções avançadas de caractere.) No entanto, se você consultar a propriedade quando a fala estiver desabilitada, o servidor não iniciará os serviços de fala.

Essa propriedade só se aplica ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

## <a name="see-also"></a>Consulte Também

[**Método de escuta**](listen-method.md)


 

 





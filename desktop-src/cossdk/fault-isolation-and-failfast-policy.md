---
description: Política de FailFast e isolamento de falhas
ms.assetid: 219c417c-a8a1-49eb-bc5a-702a16994d66
title: Política de FailFast e isolamento de falhas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc097a6d45f10d4ef8a8d059b1376862edd785ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500895"
---
# <a name="fault-isolation-and-failfast-policy"></a>Política de FailFast e isolamento de falhas

O COM+ executa amplas verificações de consistência e integridade interna. Se o COM+ encontrar uma condição de erro interno inesperada, ele encerrará imediatamente o processo. Essa política, chamada *FailFast*, facilita a contenção de falhas e resulta em sistemas mais confiáveis e robustos.

Considere um caso em que o COM+ detecta que uma de suas estruturas de dados está em um estado corrompido. Neste ponto, a causa e a magnitude da corrupção são desconhecidas e, infelizmente, o COM+ não pode dizer até que distância o dano se espalha. No entanto, embora o COM+ esteja em um estado indeterminado, ele não é executado isoladamente. Assim como outras DLLs, ela é hospedada em um ambiente de processo e compartilha um único espaço de endereço com o executável do programa principal e muitas outras DLLs. Portanto, o COM+ pressupõe que todo o processo foi corrompido, e o processo é imediatamente encerrado para impedir que ele espalhe informações potencialmente corrompidas para outros processos ou, pior ainda, de permitir que os dados corrompidos sejam confirmados e tornados duráveis.

COM+ não permite que exceções se propaguem fora de um contexto. Se ocorrer uma exceção durante a execução em um contexto COM+ e o aplicativo não capturar a exceção antes de retornar do contexto, o COM+ capturará a exceção e encerrará o processo. Usar a política FailFast nesse caso se baseia na suposição de que a exceção colocou o processo em um estado indeterminado; Não é seguro continuar o processamento.

Como desenvolvedor ou administrador, você deve inspecionar o log do aplicativo Visualizador de Eventos para obter detalhes sobre qualquer ação de FailFast ou erros graves de aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Localizando a origem de um erro](finding-the-source-of-an-error.md)
</dt> <dt>

[Como o COM+ modifica valores de retorno](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretando códigos de erro](interpreting-error-codes.md)
</dt> <dt>

[Estratégias para lidar com erros no COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Solução de problemas](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 




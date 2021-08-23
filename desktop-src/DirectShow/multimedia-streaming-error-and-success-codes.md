---
description: Erros de streaming multimídia e códigos de êxito
ms.assetid: 3b7a11d2-55b9-4505-8eb2-46be423c662b
title: Erros de streaming multimídia e códigos de êxito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d1a943ed4d41acd712ad19680e896df33b3afe2ed733bad86a129e2993e6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952195"
---
# <a name="multimedia-streaming-error-and-success-codes"></a>Erros de streaming multimídia e códigos de êxito

> [!Note]  
> Essa API está preterida. Novos aplicativos não devem usá-lo.

 

A lista a seguir contém mensagens de erro e notificações de êxito para aplicativos que usam as interfaces de streaming multimídia. Essa lista não contém todos os erros possíveis; os erros mostrados se aplicam especificamente à implementação ® DirectShow® Microsoft das interfaces de streaming multimídia.



| Valor                       | Código hexadecimal | Descrição                                                                                                                                                                                |
|-----------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MS \_ S \_ PENDENTE              | 0x00040001       | A atualização de exemplo ainda não foi concluída.                                                                                                                                                         |
| \_NOUPDATE DO MS \_             | 0x00040002       | O exemplo não foi atualizado após a conclusão forçada.                                                                                                                                            |
| MS \_ S \_ ENDOFSTREAM          | 0x00040003       | Fim do fluxo. Amostra não atualizada.                                                                                                                                                         |
| MS \_ E \_ SAMPLEALLOC          | 0x80040401       | Não foi possível remover um objeto [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) de um [**objeto IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) porque ele ainda contém pelo menos um exemplo alocado. |
| MS \_ E \_ PURPOSEID            | 0x80040402       | A ID de finalidade especificada não pode ser usada para a chamada.                                                                                                                                       |
| MS \_ E \_ NOSTREAM             | 0x80040403       | Nenhum fluxo pode ser encontrado com os atributos especificados.                                                                                                                                      |
| MS \_ \_ EEKING            | 0x80040404       | Não há suporte para esse objeto [**IMultiMediaStream.**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream)                                                                                                      |
| MS \_ E \_ INCOMPATÍVEL         | 0x80040405       | Os formatos de fluxo não são compatíveis.                                                                                                                                                     |
| MS \_ E \_ BUSY                 | 0x80040406       | O exemplo está ocupado.                                                                                                                                                                        |
| MS \_ E \_ NOTINIT              | 0x80040407       | O objeto não pode aceitar a chamada porque sua função de inicialização ou equivalente não foi chamada.                                                                                        |
| MS \_ E \_ SOURCEALREADYDEFINED | 0x80040408       | Origem já definida.                                                                                                                                                                    |
| MS \_ E \_ INVALIDSTREAMTYPE    | 0x80040409       | O tipo de fluxo não é válido para esta operação.                                                                                                                                           |
| MS \_ E \_ NOTRUNNING           | 0x8004040A       | O [**objeto IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) não está em estado de execução.                                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Streaming multimídia](multimedia-streaming.md)
</dt> </dl>

 

 




---
description: Erros de streaming de multimídia e códigos de êxito
ms.assetid: 3b7a11d2-55b9-4505-8eb2-46be423c662b
title: Erros de streaming de multimídia e códigos de êxito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c54a185b46134f4603c7adea0f1b4467da3a2cf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297988"
---
# <a name="multimedia-streaming-error-and-success-codes"></a>Erros de streaming de multimídia e códigos de êxito

> [!Note]  
> Essa API está preterida. Novos aplicativos não devem usá-lo.

 

A lista a seguir contém mensagens de erro e notificações de êxito para aplicativos que usam interfaces de streaming de multimídia. Esta lista não contém todos os erros possíveis; os erros mostrados se aplicam especificamente à implementação do Microsoft® DirectShow® das interfaces de streaming de multimídia.



| Valor                       | Código hexadecimal | Descrição                                                                                                                                                                                |
|-----------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MS \_ S \_ pendente              | 0x00040001       | A atualização de exemplo ainda não foi concluída.                                                                                                                                                         |
| noupdate do MS \_ S \_             | 0x00040002       | O exemplo não foi atualizado após a conclusão forçada.                                                                                                                                            |
| \_ENDOFSTREAM MS S \_          | 0x00040003       | Fim do fluxo. Exemplo não atualizado.                                                                                                                                                         |
| MS \_ E \_ SAMPLEALLOC          | 0x80040401       | Um objeto [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) não pôde ser removido de um objeto [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) porque ele ainda contém pelo menos um exemplo alocado. |
| MS \_ E \_ purposeid            | 0x80040402       | A ID de finalidade especificada não pode ser usada para a chamada.                                                                                                                                       |
| MS \_ E \_ nostream             | 0x80040403       | Nenhum fluxo pode ser encontrado com os atributos especificados.                                                                                                                                      |
| MS \_ E \_ nobuscando            | 0x80040404       | A busca não tem suporte para este objeto [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) .                                                                                                      |
| MS \_ E \_ incompatível         | 0x80040405       | Os formatos de fluxo não são compatíveis.                                                                                                                                                     |
| MS \_ E \_ Busy                 | 0x80040406       | O exemplo está ocupado.                                                                                                                                                                        |
| MS \_ E não \_ init              | 0x80040407       | O objeto não pode aceitar a chamada porque sua função de inicialização ou equivalente não foi chamada.                                                                                        |
| MS \_ E \_ SOURCEALREADYDEFINED | 0x80040408       | Fonte já definida.                                                                                                                                                                    |
| MS \_ E \_ INVALIDSTREAMTYPE    | 0x80040409       | O tipo de fluxo não é válido para esta operação.                                                                                                                                           |
| MS \_ E não \_ running           | 0x8004040A       | O objeto [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) não está em estado de execução.                                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Streaming de multimídia](multimedia-streaming.md)
</dt> </dl>

 

 




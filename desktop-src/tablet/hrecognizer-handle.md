---
description: Um identificador HRECOGNIZER é usado para criar um contexto de reconhecedor, recuperar os atributos e as propriedades do reconhecedor e determinar quais propriedades de pacote o reconhecedor exige para executar o reconhecimento.
ms.assetid: 1fc1901e-8c4d-4ef1-8c38-52d46ce10a48
title: Identificador HRECOGNIZER (recapitular. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 192890991dcb7e8b0a0086bbca68a6ccbc2af790d9c7d78e76fe963d268c8240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092446"
---
# <a name="hrecognizer-handle"></a>Identificador de HRECOGNIZER

Um identificador **HRECOGNIZER** é usado para criar um contexto de reconhecedor, recuperar os atributos e as propriedades do reconhecedor e determinar quais propriedades de pacote o reconhecedor exige para executar o reconhecimento.


```C++
typedef HANDLE HRECOGNIZER;
```



## <a name="remarks"></a>Comentários

As funções a seguir usam um **HRECOGNIZER**.



| Função                                                               | Descrição                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**Recognizer**](/windows/desktop/api/recapis/nf-recapis-createrecognizer)                           | Cria um reconhecedor.<br/>                                                                   |
| [**DestroyRecognizer**](/windows/desktop/api/recapis/nf-recapis-destroyrecognizer)                         | Destrói um reconhecedor.<br/>                                                                  |
| [**GetRecoAttributes**](/windows/desktop/api/recapis/nf-recapis-getrecoattributes)                         | Retorna os atributos do reconhecedor.<br/>                                               |
| [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext)                                 | Cria um contexto de reconhecedor.<br/>                                                           |
| [**DestroyContext**](/windows/desktop/api/recapis/nf-recapis-destroycontext)                               | Destrói um contexto de reconhecedor.<br/>                                                          |
| [**GetAllRecognizers**](/windows/desktop/api/recapis/nf-recapis-getallrecognizers)                         | Obtém todos os reconhecedores.<br/>                                                                   |
| [**GetResultPropertyList**](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)                 | Recupera uma lista de propriedades que o reconhecedor pode retornar para um intervalo de resultados.<br/>            |
| [**GetPreferredPacketDescription**](/windows/desktop/api/recapis/nf-recapis-getpreferredpacketdescription) | Recupera uma descrição de pacote que contém as propriedades de pacote que o reconhecedor usa.<br/> |
| [**GetUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-getunicoderanges)                           | Recupera os intervalos de pontos Unicode que o reconhecedor dá suporte.<br/>                    |
| [**LoadCachedAttributes**](/windows/desktop/api/recapis/nf-recapis-loadcachedattributes)                   | Carrega os atributos armazenados em cache de um reconhecedor.<br/>                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                        |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| Cabeçalho<br/>                   | <dl> <dt>Recapitular. h</dt> </dl> |



 

 





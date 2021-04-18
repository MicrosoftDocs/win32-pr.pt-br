---
description: A enumeração do conjunto de caracteres de BLOB \_ \_ indica o conjunto de caracteres usado pelo blob de conferência atual.
ms.assetid: 79131b84-19b5-492b-a44e-9d47c365b298
title: Enumeração de BLOB_CHARACTER_SET (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b180a8574f1643a5fc1be134be99c951faaf1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811935"
---
# <a name="blob_character_set-enumeration"></a>Enumeração do conjunto de \_ caracteres do blob \_

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A enumeração do **\_ \_ conjunto de caracteres de blob** indica o conjunto de caracteres usado pelo blob de conferência atual.

## <a name="syntax"></a>Syntax


```C++
} BLOB_CHARACTER_SET;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**ASCII do BCS \_**
</dt> <dd>

Formato ASCII padrão.

</dd> <dt>

<span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**UTF7 de BCS \_**
</dt> <dd>

Formato de transformação de sete bits do Unicode. Para obter detalhes sobre esse formato, realize uma pesquisa na Internet para o RFC 1642.

</dd> <dt>

<span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**BCS \_ UTF8**
</dt> <dd>

Formato de transformação UCS 8. Para obter detalhes sobre esse formato, realize uma pesquisa na Internet para ISO (o Organização Internacional de Normalização) e o IEC (o International Electrotechnical Commission) Document ISO/IEC JTC1/SC2/WG2 N 1036, com data de 1º de agosto de 1994, por WG2 Project editor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                               |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> <dt>

[**obter \_ CharacterSet**](itconferenceblob-get-characterset.md)
</dt> <dt>

[**Init**](itconferenceblob-init.md)
</dt> <dt>

[**SetConferenceBlob**](itconferenceblob-setconferenceblob.md)
</dt> </dl>

 

 





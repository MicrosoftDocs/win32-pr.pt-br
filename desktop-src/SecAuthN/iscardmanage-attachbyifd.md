---
description: Cria um link de comunicação para um leitor, usando um nome de exibição fornecido para o leitor.
ms.assetid: 7916896b-c460-47b2-a1db-17d8fc9bdd2e
title: 'Método ISCardManage:: AttachByIFD'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByIFD
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae0aaae2157331d5d1bae2814c563c89dc73c757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749480"
---
# <a name="iscardmanageattachbyifd-method"></a>Método ISCardManage:: AttachByIFD

\[O método **AttachByIFD** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **AttachByIFD** cria um link de comunicação para um [*leitor*](../secgloss/r-gly.md), usando um nome de exibição fornecido para o leitor.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AttachByIFD(
  [in] BSTR bstrIFDName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrIFDName* \[ no\]
</dt> <dd>

O nome de exibição do leitor.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis:



| Código de retorno                                                                                   | Descrição                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *bstrIFDName* não é válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                            |



 

## <a name="remarks"></a>Comentários

Para anexar uma chamada de [*cartão inteligente*](../secgloss/s-gly.md) [**AttachByHandle**](iscardmanage-attachbyhandle.md).

Para liberar uma chamada de anexo, [**desanexar**](iscardmanage-detach.md).

Para se reconectar com o cartão inteligente sem chamar [**Detach**](iscardmanage-detach.md) e **AttachByIFD**, chame [**reconnect**](iscardmanage-reconnect.md).

Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardManage**](iscardmanage.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AttachByHandle**](iscardmanage-attachbyhandle.md)
</dt> <dt>

[**Detach**](iscardmanage-detach.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**Reconectar**](iscardmanage-reconnect.md)
</dt> </dl>

 

 

---
description: Cria um link de comunicação para um cartão inteligente (ICC) usando um alçamento retornado pelo gerenciador de recursos de cartão inteligente.
ms.assetid: dfd05dce-4416-4881-92ca-c85baccf3b86
title: Método ISCardManage::AttachByHandle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByHandle
api_type:
- COM
api_location: ''
ms.openlocfilehash: c464f2d514a59754b5dc4d9d98f745a4802843c3cfafa3df16057c53456221c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014156"
---
# <a name="iscardmanageattachbyhandle-method"></a>Método ISCardManage::AttachByHandle

\[O **método AttachByHandle** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método AttachByHandle** cria um link de comunicação para um cartão inteligente (ICC) usando um handle retornado pelo gerenciador de recursos [*de cartão inteligente*](../secgloss/r-gly.md). [](../secgloss/s-gly.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AttachByHandle(
  [in] HSCARD hICC
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hICC* \[ Em\]
</dt> <dd>

Um handle para um cartão inteligente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis:



| Código de retorno                                                                                   | Descrição                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O *parâmetro hICC* não é válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                     |



 

## <a name="remarks"></a>Comentários

Para anexar uma [*chamada de*](../secgloss/r-gly.md) leitor [**AttachByIFD.**](iscardmanage-attachbyifd.md)

Para liberar uma chamada de anexo [**Desconectar**](iscardmanage-detach.md).

Para se reconectar com o cartão inteligente sem chamar [**Detach**](iscardmanage-detach.md) e **AttachByHandle,** chame [**Reconectar**](iscardmanage-reconnect.md).

Para ver uma lista de todos os métodos definidos pela interface [**ISCardManage,**](iscardmanage.md) [**consulte ISCardManage**](iscardmanage.md).

Além dos códigos de erro COM listados acima, essa interface poderá retornar um código de erro de cartão inteligente se uma função de cartão inteligente tiver sido chamada para concluir a solicitação. Para obter informações sobre códigos de erro de cartão inteligente, consulte [Valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AttachByIFD**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**Detach**](iscardmanage-detach.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**Reconectar**](iscardmanage-reconnect.md)
</dt> </dl>

 

 

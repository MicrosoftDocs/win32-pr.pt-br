---
description: O método Seek seleciona o objeto do qual o acesso (leitura/gravação) será feito.
ms.assetid: 9e06df70-6415-46dd-b34f-59614d1cbee7
title: 'Método ISCardFileAccess:: Seek'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Seek
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5f4059eb2943411cfa5a3fb2b2ae247cd0fda7dd735cc1f1f61d516181976b6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923155"
---
# <a name="iscardfileaccessseek-method"></a>Método ISCardFileAccess:: Seek

\[O método **Seek** está disponível para uso nos sistemas operacionais especificados na seção requisitos. ele não está disponível para uso no Windows server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **Seek** seleciona o objeto do qual o acesso (leitura/gravação) será feito.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Seek(
  [in] HSCARD_FILE hFile,
  [in] SEEKTYPE    *Seek,
  [in] LONG        lOffset 
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFile* \[ no\]
</dt> <dd>

Identificador do arquivo aberto.

</dd> <dt>

*Buscar* \[ no\]
</dt> <dd>

Local em que a busca deve começar.



| Valor                                                                                                | Significado                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>SC \_ Seek \_ do \_ início</dt> </dl> | Comece a pesquisa no início.<br/>          |
| <dl> <dt>SC \_ Seek \_ do \_ final </dt> </dl>      | Comece a pesquisa a partir do final.<br/>              |
| <dl> <dt>SC \_ Seek \_ relativo</dt> </dl>        | Comece a Pesquisar a partir da posição atual.<br/> |



 

</dd> <dt>

*lOffset* \[ no\]
</dt> <dd>

Número de objetos de dados do objeto de referência.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parâmetro inválido.<br/>                |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                    |



 

## <a name="remarks"></a>Comentários

Para ler ou gravar um arquivo, chame [**Read**](iscardfileaccess-read.md) ou [**Write**](iscardfileaccess-write.md) respectivamente.

Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/> |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> <dt>

[**Ler**](iscardfileaccess-read.md)
</dt> <dt>

[**Gravar**](iscardfileaccess-write.md)
</dt> </dl>

 

 

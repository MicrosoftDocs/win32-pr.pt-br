---
description: O método de diretório recupera uma lista de arquivos do tipo especificado do diretório atual.
ms.assetid: 0ae89811-7534-497b-af9f-ae37a48bc3e5
title: 'ISCardFileAccess: método diretório de:D'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Directory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 74293d4fa97a61133739cac75f17eaffed6e52b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827854"
---
# <a name="iscardfileaccessdirectory-method"></a>ISCardFileAccess: método diretório de:D

\[O método de **diretório** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método de **diretório** recupera uma lista de arquivos do tipo especificado do diretório atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Directory(
  [in]  FILETYPE    fileType,
  [out] LPSAFEARRAY *ppFileList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*filetype* \[ no\]
</dt> <dd>

Tipo de arquivos de [*cartão inteligente*](../secgloss/s-gly.md) a serem listados.



| Valor                                                                                                                                                                                      | Significado                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="SC_TYPE_DIRECTORIES"></span><span id="sc_type_directories"></span><dl> <dt>**\_diretórios do tipo SC \_**</dt> </dl>           | Listar somente arquivos de diretório.<br/>                |
| <span id="SC_TYPE_FILES"></span><span id="sc_type_files"></span><dl> <dt>**\_arquivos do tipo SC \_**</dt> </dl>                             | Listar somente arquivos elementares.<br/>               |
| <span id="SC_TYPE_ALL_FILES"></span><span id="sc_type_all_files"></span><dl> <dt>**SC \_ digite \_ todos os \_ arquivos**</dt> </dl>                | Listar os arquivos de diretório e elementares.<br/> |
| <span id="SC_TYPE_DIRECTORY_FILE"></span><span id="sc_type_directory_file"></span><dl> <dt>**\_arquivo de \_ diretório do tipo SC \_**</dt> </dl> | Arquivo de diretório.<br/>                           |
| <span id="SC_TYPE_TRANSPARENT_EF"></span><span id="sc_type_transparent_ef"></span><dl> <dt>**SC \_ tipo \_ transparente \_ EF**</dt> </dl> | Arquivo elementar transparente.<br/>              |
| <span id="SC_TYPE_FIXED_EF"></span><span id="sc_type_fixed_ef"></span><dl> <dt>**\_tipo SC \_ Fixed \_ EF**</dt> </dl>                   | Arquivo elementar fixo linear.<br/>             |
| <span id="SC_TYPE_CYCLIC_EF"></span><span id="sc_type_cyclic_ef"></span><dl> <dt>**SC \_ tipo \_ cíclico de \_ EF**</dt> </dl>                | Arquivo de elementar cíclico.<br/>                   |
| <span id="SC_TYPE_VARIABLE_EF"></span><span id="sc_type_variable_ef"></span><dl> <dt>**SC \_ Type \_ variável \_ EF**</dt> </dl>          | Arquivo elementar variável linear.<br/>          |



 

</dd> <dt>

*ppFileList* \[ fora\]
</dt> <dd>

Matriz de BSTRs que representa a lista de arquivos que correspondem ao especificador em *filetype*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | A operação foi concluída com êxito.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parâmetro inválido.<br/>                             |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | A interface não implementou este método.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                                 |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado para *ppFileList*.<br/>  |



 

## <a name="remarks"></a>Comentários

Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).

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

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 

---
description: O método Directory recupera uma lista de arquivos do tipo especificado do diretório atual.
ms.assetid: 0ae89811-7534-497b-af9f-ae37a48bc3e5
title: Método ISCardFileAccess::D irectory
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
ms.openlocfilehash: 009263a92f014367636c7ff16b7f43635f73fa1b2ed17b52d53e81152c6e15b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481296"
---
# <a name="iscardfileaccessdirectory-method"></a>Método ISCardFileAccess::D irectory

\[O **método** Directory está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método** Directory recupera uma lista de arquivos do tipo especificado do diretório atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Directory(
  [in]  FILETYPE    fileType,
  [out] LPSAFEARRAY *ppFileList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fileType* \[ Em\]
</dt> <dd>

Tipo de [*arquivos de cartão inteligente*](../secgloss/s-gly.md) a listar.



| Valor                                                                                                                                                                                      | Significado                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="SC_TYPE_DIRECTORIES"></span><span id="sc_type_directories"></span><dl> <dt>**DIRETÓRIOS \_ DE \_ TIPO SC**</dt> </dl>           | Listar somente arquivos de diretório.<br/>                |
| <span id="SC_TYPE_FILES"></span><span id="sc_type_files"></span><dl> <dt>**ARQUIVOS \_ DE TIPO \_ SC**</dt> </dl>                             | Lista somente arquivos elementares.<br/>               |
| <span id="SC_TYPE_ALL_FILES"></span><span id="sc_type_all_files"></span><dl> <dt>**SC \_ DIGITE TODOS OS \_ \_ ARQUIVOS**</dt> </dl>                | Liste os arquivos de diretório e elementares.<br/> |
| <span id="SC_TYPE_DIRECTORY_FILE"></span><span id="sc_type_directory_file"></span><dl> <dt>**SC \_ TYPE \_ DIRECTORY \_ FILE**</dt> </dl> | Arquivo de diretório.<br/>                           |
| <span id="SC_TYPE_TRANSPARENT_EF"></span><span id="sc_type_transparent_ef"></span><dl> <dt>**SC \_ TYPE \_ TRANSPARENT \_ EF**</dt> </dl> | Arquivo elementar transparente.<br/>              |
| <span id="SC_TYPE_FIXED_EF"></span><span id="sc_type_fixed_ef"></span><dl> <dt>**EF \_ FIXO DO TIPO \_ \_ SC**</dt> </dl>                   | Arquivo elementar fixo linear.<br/>             |
| <span id="SC_TYPE_CYCLIC_EF"></span><span id="sc_type_cyclic_ef"></span><dl> <dt>**SC \_ TYPE \_ CYCLIC \_ EF**</dt> </dl>                | Arquivo elementar cíclico.<br/>                   |
| <span id="SC_TYPE_VARIABLE_EF"></span><span id="sc_type_variable_ef"></span><dl> <dt>**SC \_ TYPE \_ VARIABLE \_ EF**</dt> </dl>          | Arquivo elementar de variável linear.<br/>          |



 

</dd> <dt>

*ppFileList* \[ out\]
</dt> <dd>

Matriz de BSTRs que representa a lista de arquivos correspondentes ao especificador em *fileType*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | A operação foi concluída com êxito.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parâmetro inválido.<br/>                             |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | A interface não implementou esse método.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                                 |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | Um ponteiro ruim foi passado para *ppFileList.*<br/>  |



 

## <a name="remarks"></a>Comentários

Para ver uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).

Além dos códigos de erro COM listados acima, essa interface poderá retornar um código de erro de cartão inteligente se uma função de cartão inteligente tiver sido chamada para concluir a solicitação. Para obter mais informações, consulte [Valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 

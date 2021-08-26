---
description: A função DeletePrinterDriverEx remove o nome de driver de impressora especificado da lista de nomes de drivers com suporte em um servidor e exclui os arquivos associados ao driver. Essa função também pode excluir versões específicas do driver.
ms.assetid: 1a3d7c7f-1d45-4877-a8f7-a77f40e3c319
title: Função DeletePrinterDriverEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverEx
- DeletePrinterDriverExA
- DeletePrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 88cc39227ffc5b1700a1348541e18215bc10c8b87a6bff942611f098059a70e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950036"
---
# <a name="deleteprinterdriverex-function"></a>Função DeletePrinterDriverEx

A função **DeletePrinterDriverEx** remove o nome de driver de impressora especificado da lista de nomes de drivers com suporte em um servidor e exclui os arquivos associados ao driver. Essa função também pode excluir versões específicas do driver.

## <a name="syntax"></a>Sintaxe


```C++
BOOL DeletePrinterDriverEx(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName,
  _In_ DWORD  dwDeleteFlag,
  _In_ DWORD  dwVersionFlag
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor do qual o driver deve ser excluído. Se esse parâmetro for **nulo**, a função excluirá o driver de impressora do computador local.

</dd> <dt>

*pEnvironment* \[ no\]
</dt> <dd>

um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente do qual o driver deve ser excluído (por exemplo, Windows NT x86, Windows IA64 ou Windows x64). Se esse parâmetro for **nulo**, o nome do driver será excluído do ambiente atual do aplicativo de chamada e do computador cliente (não do aplicativo de destino e do servidor de impressão).

</dd> <dt>

*pDriverName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver a ser excluído.

</dd> <dt>

*dwDeleteFlag* \[ no\]
</dt> <dd>

As opções para excluir arquivos e versões do driver. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                     | Significado                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DPD_DELETE_SPECIFIC_VERSION"></span><span id="dpd_delete_specific_version"></span><dl> <dt>**DPD \_ excluir \_ \_ versão específica**</dt> </dl> | Exclui a versão especificada em *dwVersionFlag*. Isso não garante que o driver será removido da lista de drivers com suporte para o servidor.<br/>                  |
| <span id="DPD_DELETE_UNUSED_FILES"></span><span id="dpd_delete_unused_files"></span><dl> <dt>**DPD \_ excluir \_ arquivos não utilizados \_**</dt> </dl>             | Remove todos os arquivos de driver não utilizados.<br/>                                                                                                                                           |
| <span id="DPD_DELETE_ALL_FILES"></span><span id="dpd_delete_all_files"></span><dl> <dt>**DPD \_ excluir \_ todos os \_ arquivos**</dt> </dl>                      | Excluirá o driver somente se todos os seus arquivos associados puderem ser removidos. A operação de exclusão falhará se qualquer um dos arquivos do driver estiver sendo usado por algum outro driver instalado.<br/> |



 

Se DPD \_ excluir \_ \_ versão específica não for especificado, a função excluirá todas as versões do driver se nenhuma delas estiver em uso. Se nem DPD \_ excluir \_ arquivos não utilizados \_ nem DPD \_ excluir \_ todos os \_ arquivos for especificado, a função não excluirá os arquivos de driver.

</dd> <dt>

*dwVersionFlag* \[ no\]
</dt> <dd>

A versão do driver a ser excluído. Esse parâmetro pode ser 0, 1, 2 ou 3. Esse parâmetro será usado somente se *dwDeleteFlag* incluir o \_ sinalizador de versão específica de exclusão de DPD \_ \_ .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Antes que a função exclua os arquivos de driver, ele chama a função **DrvDriverEvent** do driver, permitindo que o driver remova todos os arquivos privados que não são usados. para obter mais informações sobre o **DrvDriverEvent**, consulte o Microsoft Windows Driver Development Kit (DDK).

Se os arquivos de driver estiverem carregados no momento, a função os moverá para um diretório temporário e os marcará para exclusão na reinicialização.

Antes de chamar **DeletePrinterDriverEx**, você deve excluir todos os objetos de impressora que usam o driver de impressora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **DeletePrinterDriverExW** (Unicode) e **DeletePrinterDriverExA** (ANSI)<br/>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> </dl>

 

 





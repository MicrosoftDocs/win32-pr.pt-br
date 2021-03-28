---
description: Inicia o assistente do Passport quando usado com Rundll32.exe.
title: Função PassportWizardRunDll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PassportWizardRunDll
api_type:
- DllExport
api_location:
- Netplwiz.dll
ms.assetid: 015c3875-698e-4d80-bbfc-4fc8a71197b7
ms.openlocfilehash: a858a36caa4af8095fc7023abae5ad918321f53e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170094"
---
# <a name="passportwizardrundll-function"></a>Função PassportWizardRunDll

\[Essa função está disponível por meio do Windows XP com Service Pack 2 (SP2) e Windows Server 2003. Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.\]

Inicia o assistente do Passport quando usado com Rundll32.exe.

## <a name="syntax"></a>Sintaxe


```C++
void PassportWizardRunDll(
  _In_ HWND      hwndStub,
  _In_ HINSTANCE hAppInstance,
  _In_ LPTSTR    lpszCmdLine,
  _In_ int       nCmdShow
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndStub* \[ no\]
</dt> <dd>

Tipo: **HWND**

Um identificador para uma janela do proprietário. Esse parâmetro é normalmente definido como **nulo**.

</dd> <dt>

*hAppInstance* \[ no\]
</dt> <dd>

Tipo: **HINSTANCE**

Um identificador para o arquivo de biblioteca, obtido como um valor de retorno de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").

</dd> <dt>

*lpszCmdLine* \[ no\]
</dt> <dd>

Tipo: **LPTSTR**

Dados de argumento. Esse valor sempre estará vazio.

</dd> <dt>

*nCmdShow* \[ no\]
</dt> <dd>

Tipo: **int**

Define o modo de exibição para a janela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Nenhum.

## <a name="remarks"></a>Comentários

O assistente do Passport é usado para obter um Passport padrão do Windows. Um Passport fornece ao usuário acesso personalizado a todos os sites do MSN e outros sites habilitados para Passport usando o endereço de email do usuário. O uso de **PassportWizardRunDll** como um ponto de entrada no arquivo de Netplwiz.dll por meio de um comando rundll32 permite iniciar o assistente do Passport a partir de uma linha de comando como se fosse um arquivo executável.

**PassportWizardRunDll** é usado exclusivamente no contexto de um comando Rundll32.exe da seguinte maneira:

**rundll32.exe netplwiz.dll, PassportWizardRunDll**

O uso de uma função de ponto de entrada com Rundll32.exe não se assemelha a uma chamada de função normal. O nome da função e o nome do arquivo. dll onde ele está armazenado são usados apenas como parâmetros de linha de comando. A definição de função mostrada em sintaxe é apenas um protótipo padrão para todas as funções que você pode chamar usando rundll32. Os valores específicos para *hwndStub*, *hAppInstance* e *nCmdShow* não são fornecidos pelo usuário, mas são tratados em segundo plano por rundll32. **PassportWizardRunDll** não usa o valor *lpszCmdLine* , portanto, nenhum dado adicional é necessário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                            |
| parâmetro<br/>                   | <dl> <dt>Nenhum</dt> </dl>                                 |
| DLL<br/>                      | <dl> <dt>Netplwiz.dll (versão 5,60 ou posterior)</dt> </dl> |



 

 

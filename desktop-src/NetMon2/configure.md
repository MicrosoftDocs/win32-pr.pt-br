---
description: Configura o especialista na DLL especialista.
ms.assetid: 3906569d-9ad4-4c03-9637-f4a57697b227
title: Configurar a função de retorno de chamada (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Configure
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 528e83c72b015bdac288b9e2c7e4838f665c92991f83c6f1eb105d454cb6ac74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064147"
---
# <a name="configure-callback-function"></a>Configurar função de retorno de chamada

A **função Configurar** configura o especialista na DLL especialista.

O especialista deve implementar a **função Configurar.** Quando a chamada de função é recebida, o especialista exibe uma caixa de diálogo que permite que o usuário altere qualquer item configurável.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI Configure(
  _In_    HEXPERTKEY         hExpertKey,
  _Inout_ PEXPERTCONFIG      *ppConfig,
  _In_    PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_    DWORD              StartupFlags,
  _In_    HWND               hWnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hExpertKey* \[ Em\]
</dt> <dd>

Identificador de especialista exclusivo.

O identificador exclusivo é passado de volta em todas as funções específicas Monitor de Rede especialistas. Esteja ciente de que o identificador pode não ser a mesma chave de especialista que a passada para a [**função**](run.md) Executar. Não armazene a chave de especialista na **chamada Configurar.**

</dd> <dt>

*ppConfig* \[ in, out\]
</dt> <dd>

Um ponteiro para um ponteiro para uma estrutura [**EXPERTCONFIG**](expertconfig.md) na entrada.

Após uma saída bem-sucedida, a estrutura [**EXPERTCONFIG referenciada**](expertconfig.md) contém os novos dados de configuração.

</dd> <dt>

*pExpertStartupInfo* \[ Em\]
</dt> <dd>

Um ponteiro para o elemento de captura com foco quando o especialista foi iniciado.

</dd> <dt>

*StartupFlags* \[ Em\]
</dt> <dd>

Os sinalizadores que indicam como o especialista deve usar o *parâmetro pExpertStartupInfo.* O único sinalizador definido é **EXPERT STARTUP FLAG USE STARTUP DATA OVER \_ \_ \_ \_ \_ \_ \_ CONFIG \_ DATA**. O sinalizador indica que o especialista usará o parâmetro *pExpertStartupInfo* em vez do *parâmetro ppConfig* passado. Normalmente, você definirá o sinalizador ao iniciar o especialista em um menu de contexto.

</dd> <dt>

*hWnd* \[ Em\]
</dt> <dd>

Um alça para a janela pai. Use o alça para abrir uma caixa de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida (ou seja, se houver uma configuração atual), o valor de retorno será **TRUE.**

Se a função não for bem-sucedida, o valor de retorno será **FALSE.**

## <a name="remarks"></a>Comentários

Monitor de Rede chama a **função Configurar** com a configuração atual do especialista, se houver. O especialista exibe uma caixa de diálogo, com a qual você pode alterar qualquer item configurável.

Quando *ppConfig* é passado e Monitor de Rede não tem uma configuração armazenada para o especialista especificado, o valor do parâmetro pode ser **NULL.** Nesse caso, a **função Configurar** assume valores padrão codificados (ou, usa as informações de inicialização) para abrir a caixa de diálogo.

Os dados de configuração também podem ser **NULL** quando a **função Configure** retorna e um **NULL** foi passado. Essa situação ocorre quando Monitor de Rede não tem um padrão armazenado e o usuário pressiona **Cancelar**.

O início da estrutura [**de dados EXPERTCONFIG**](expertconfig.md) inclui uma seção Privada que armazena as informações de tamanho da estrutura. O tamanho da estrutura **EXPERTCONFIG** deve incluir o comprimento **DWORD** reservado que aparece no início da estrutura. Por exemplo, se os dados de configuração exigirem 20 bytes de espaço de armazenamento, aloce 24 bytes para armazenar os dados. Se um *ppConfig* for **NULL,** a função **Configure** chamará a função [**ExpertAllocMemory**](expertallocmemory.md) para alocar uma nova configuração com o tamanho correto. Se o buffer não for suficiente para manter os dados de especialistas, o especialista deverá chamar a função [**ExpertReallocMemory.**](expertreallocmemory.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 





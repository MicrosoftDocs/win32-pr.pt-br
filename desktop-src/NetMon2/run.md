---
description: O especialista deve implementar a função Run. Monitor de Rede chama a função executar para iniciar o especialista na DLL do especialista.
ms.assetid: 9ef3941b-d9e9-4acb-97ed-5f39573f2946
title: Executar função de retorno de chamada (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Run
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: e31c5c729bba133fa4c4d3e36bbc54035a274923a03a8718acf05a601192775b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074496"
---
# <a name="run-callback-function"></a>Executar função de retorno de chamada

O especialista deve implementar a função **Run** . Monitor de Rede chama a função **executar** para iniciar o especialista na DLL do especialista.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI Run(
  _In_ HEXPERTKEY         hExpertKey,
  _In_ PEXPERTCONFIG      pConfig,
  _In_ PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_ DWORD              StartupFlags,
  _In_ HWND               hWndParent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hExpertKey* \[ no\]
</dt> <dd>

Identificador exclusivo do especialista que é passado de volta para todas as funções de Monitor de Rede específicas do especialista.

> [!Note]  
> O identificador *hExpertKey* pode passar uma chave de especialista diferente da chave de especialista que a função [**Configurar**](configure.md) passa.

 

</dd> <dt>

*pConfig* \[ no\]
</dt> <dd>

Ponteiro para a configuração existente. O parâmetro *pConfig* pode ser **nulo** , o que significa que o especialista pode ser executado com padrões embutidos em código ou informações de inicialização às quais o parâmetro *pExpertStartupInfo* faz referência.

</dd> <dt>

*pExpertStartupInfo* \[ no\]
</dt> <dd>

Ponteiro para o elemento capture que tem o foco quando o especialista é iniciado.

</dd> <dt>

*StartupFlags* \[ no\]
</dt> <dd>

Indicador de como o especialista deve usar o parâmetro *pExpertStartupInfo* .

O único sinalizador definido é:



| Valor                                                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EXPERT_STARTUP_FLAG_USE_STARTUP_DATA_OVER_CONFIG_DATA."></span><span id="expert_startup_flag_use_startup_data_over_config_data."></span><dl> <dt>**sinalizador de inicialização de especialista \_ \_ \_ use \_ dados de inicialização \_ \_ em \_ dados de configuração \_ .**</dt> </dl> | Esse sinalizador indica que o especialista usa o parâmetro *pExpertStartupInfo* e não usa o parâmetro *pConfig* . Normalmente, você pode definir esse sinalizador quando o especialista puder iniciar a partir de um clique com o botão direito do mouse. Se o sinalizador não estiver definido, as duas ações a seguir podem ocorrer: ou o especialista não começa com um clique com o botão direito do mouse, ou o especialista começa com um clique com o botão direito do mouse e o configura.<br/> |



 

</dd> <dt>

*hwndParent* \[ no\]
</dt> <dd>

O parâmetro *HWND* do pai (geralmente a interface do usuário monitor de rede).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida (ou seja, se o especialista for iniciado), o valor de retorno será **true**.

Se a função não for bem-sucedida, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

Durante a execução, o especialista percorre os quadros no arquivo de captura e gera um relatório ou cria eventos que mostram problemas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 





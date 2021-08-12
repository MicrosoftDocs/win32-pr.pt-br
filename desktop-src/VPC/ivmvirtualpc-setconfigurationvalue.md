---
title: Método IVMVirtualPC SetConfigurationValue (VPCCOMInterfaces.h)
description: Define o valor da definição de configuração especificada.
ms.assetid: 7760b81e-734d-4970-8875-f2d310ff6c5c
keywords:
- Pc Virtual do método SetConfigurationValue
- Método SetConfigurationValue pc virtual , interface IVMVirtualPC
- Interface IVMVirtualPC pc virtual , método SetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50d3ea585182794c1e96195fdbef842bc35c86342d390dd59e7077b31d4ef9a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591699"
---
# <a name="ivmvirtualpcsetconfigurationvalue-method"></a>Método IVMVirtualPC::SetConfigurationValue

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define o valor da definição de configuração especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    preferenceKey,
  [in] VARIANT preferenceValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*preferenceKey* \[ Em\]
</dt> <dd>

A chave usada para identificar a preferência, conforme armazenado no arquivo de configuração por usuário (Options.xml em "%LocalAppData% \\ Microsoft \\ Windows Virtual PC").

> [!IMPORTANT]
> As alterações devem ser feitas Options.xml usando o **método SetConfigurationValue.** Não há suporte Options.xml uso de qualquer outro método.

 

</dd> <dt>

*preferenceValue* \[ Em\]
</dt> <dd>

O valor de preferência. Esse valor pode ser um dos seguintes tipos **VARIANT:** **VT \_ ARRAY** \| **VT \_ UI1** (bytes brutos), **VT \_ BSTR** (cadeia de caracteres), **VT \_ UI4** (inteiro) ou **BOOL VT \_ (booliana).**

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                        | Descrição                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                                | O *parâmetro preferenceKey* ou *preferenceValue* é **NULL.**<br/>                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | O *parâmetro preferenceKey* não é válido ou é uma cadeia de caracteres vazia.<br/>                    |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Ocorreu um erro inesperado.<br/>                                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> <dt>0x80070005</dt> </dl>                           | O usuário atual não tem acesso suficiente ao arquivo de configuração.<br/>                  |
| <dl> <dt>**VM \_ VIRTUALIZAÇÃO \_ DE HARDWARE E \_ \_ DESABILITADA**</dt> <dt>0XA0040951</dt> </dl> | O processador não dá suporte a extensões de HAV (Virtualização Acelerada de Hardware).<br/> |



 

## <a name="remarks"></a>Comentários

Os valores a seguir têm suporte para o *parâmetro preferenceKey.*



| *valor preferenceKey*      | Descrição                                                                                                                                                                           | Tipo de dados            | Valor padrão   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-----------------|
| "tempo \_ de ociosidade"<br/> | Número de segundos que vpc.exe deverão esperar antes de sair se não houver VMs ou aplicativos ativos usando as [interfaces](virtual-pc-interfaces.md)de computador virtual Windows .<br/> | "integer"<br/> | "30"<br/> |



 

Esse método fornece acesso de baixo nível a qualquer valor de configuração. Ele pode ser usado para definir valores de configuração para chaves definidas pelo cliente. Tenha cuidado ao usar esse método para definir valores de configuração do sistema, pois nenhuma verificação de erro é executada no valor de configuração. Além disso, alguns valores de configuração não podem ser alterados enquanto uma máquina virtual está em execução.

As chaves de configuração estão localizadas no arquivo "Options.xml" da máquina virtual no formato XML. As chaves são armazenadas de maneira hierárquica semelhante às chaves do Registro Windows. Para especificar uma sub-chave específica, é construído um "caminho de chave" que especifica as várias chaves em um formato delimitado por marca de barra.

Por exemplo, para definir o valor da chave \_ "tempoout ocioso" localizada na árvore de chaves a seguir:

``` syntax
<preferences>
  <idle_timeout type="integer">60</idle_timeout>
```

A *cadeia de caracteres* de caminho preferenceKey seria especificada da seguinte forma:

``` syntax
"idle_timeout"
```

Se qualquer uma das chaves na árvore desejada tiver um valor de atributo "id", o atributo e seu valor são inseridos na cadeia de caracteres de caminho *preferenceKey* imediatamente após sua chave de configuração associada usando o seguinte formato entre colchetes: " \[ @id ="*id \_ value*" \] ".

Por exemplo, para definir o valor da chave "set", localizada na árvore de chaves a seguir:

``` syntax
<preferences>
  <alpha>
    <bravo>
      <charlie>
        <delta id="1">
          <echo id="0">
            <foxtrot>
              <golf type="string">D</golf>
```

A *cadeia de caracteres* de caminho preferenceKey seria especificada da seguinte forma:

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC é definido como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> <dt>

[**IVMVirtualMachine::SetConfigurationValue**](ivmvirtualmachine-setconfigurationvalue.md)
</dt> </dl>

 


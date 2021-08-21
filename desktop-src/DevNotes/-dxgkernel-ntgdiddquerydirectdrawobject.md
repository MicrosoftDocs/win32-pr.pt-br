---
description: Consulta uma representação de modo kernel criada anteriormente de um objeto Microsoft DirectDraw para seus recursos.
ms.assetid: ec07c7ef-4c57-4ed9-849b-f30692cc3181
title: Função NtGdiDdQueryDirectDrawObject (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdQueryDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 2cd87bc1cc278f8ee680dbd458ed3b92cc699a060021a91535de66996376db84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103816"
---
# <a name="ntgdiddquerydirectdrawobject-function"></a>Função NtGdiDdQueryDirectDrawObject

\[Essa função está sujeita a alterações com cada revisão do sistema operacional. Em vez disso, use o DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação diretamente com drivers de exibição.\]

Consulta uma representação de modo kernel criada anteriormente de um objeto Microsoft DirectDraw para seus recursos.

## <a name="syntax"></a>Sintaxe


```C++
BOOL APIENTRY NtGdiDdQueryDirectDrawObject(
  _In_  HANDLE                      hDirectDrawLocal,
  _Out_ DD_HALINFO                  *pHalInfo,
        DWORD                       *pCallBackFlags,
  _Out_ LPD3DNTHAL_CALLBACKS        puD3dCallbacks,
  _Out_ LPD3DNTHAL_GLOBALDRIVERDATA puD3dDriverData,
  _Out_ PDD_D3DBUFCALLBACKS         puD3dBufferCallbacks,
  _Out_ LPDDSURFACEDESC             puD3dTextureFormats,
  _Out_ DWORD                       *puNumHeaps,
  _Out_ VIDEOMEMORY                 *puvmList,
  _Out_ DWORD                       *puNumFourCC,
  _Out_ DWORD                       *puFourCC
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDirectDrawLocal* \[ Em\]
</dt> <dd>

Lidar com o dispositivo DirectDraw no modo kernel criado anteriormente.

</dd> <dt>

*pHalInfo* \[ out\]
</dt> <dd>

Ponteiro para uma [**estrutura \_ DD HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) que será preenchida com as funcionalidades do dispositivo. Confira a documentação do DDK para obter detalhes.

</dd> <dt>

*pCallBackFlags* 
</dt> <dd>

Ponteiro para um buffer fornecido pelo chamador que armazena sinalizadores de retorno de chamada relatados pelo driver. O buffer deve ser de tamanho 3 sizeof(DWORD) e armazena sinalizadores de retorno de chamada na seguinte \* ordem: pCallBackFlags 0 para sinalizadores em \[ \] [**DD \_ CALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks), pCallBackFlags 1 para sinalizadores em \[ \] [**DD \_ SURFACECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks)e pCallBackFlags 2 para sinalizadores \[ em \] [**DD \_ PALETTECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks). Confira a documentação do DDK para obter detalhes.

</dd> <dt>

*puD3dCallbacks* \[ out\]
</dt> <dd>

Ponteiro para uma tabela de ponteiros de retorno de chamada Direct3D. A tabela é preenchida com ponteiros para funções dentro Gdi32.dll que imitam um driver de exibição Direct3D. Essa tabela de retorno de chamada é idêntica à estrutura D3DHAL \_ D3DCALLBACKS discutida na documentação do DDK.

</dd> <dt>

*puD3dDriverData* \[ out\]
</dt> <dd>

Ponteiro para [**dados D3DHAL \_ GLOBALDRIVERDATA,**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) conforme descrito na documentação do DDK.

</dd> <dt>

*puD3dBufferCallbacks* \[ out\]
</dt> <dd>

Ponteiro para uma tabela de ponteiros de retorno de chamada. A tabela é preenchida com ponteiros para funções dentro Gdi32.dll que imitam um driver de exibição Direct3D. Essa tabela de retorno de chamada é idêntica à estrutura DDHAL DDEXEBUFCALLBACKS, que mapeia para a estrutura \_ [**\_ DD D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) discutida na documentação do DDK, exceto que os membros XxxD3DBuffer **em DD \_ D3DBUFCALLBACKS** são substituídos por XxxExecuteBuffer em DDHAL \_ DDEXEBUFCALLBACKS.

</dd> <dt>

*puD3dTextureFormats* \[ out\]
</dt> <dd>

Ponteiro para uma matriz de [**estruturas DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) que definem o conjunto de formatos de textura permitidos.

</dd> <dt>

*puNumHeaps* \[ out\]
</dt> <dd>

Ponteiro para o **membro dwNumHeaps** de [**DD \_ HALINFO.**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo)**vmiData**. O **membro dwNumHeaps** especifica o número de heaps de memória em *puvmList.* Confira a documentação do DDK para obter detalhes.

</dd> <dt>

*puvmList* \[ out\]
</dt> <dd>

Ponteiro para uma lista de descritores de heap de memória de vídeo. Pode ser **NULL.** Esse parâmetro não é usado porque o gerenciamento de memória de vídeo é tratado inteiramente no modo kernel.

</dd> <dt>

*puNumNumNumCc* \[ out\]
</dt> <dd>

Ponteiro para o **membro puNumCodeCCCodes** [**de DD \_ HALINFO.**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo)**ddCaps**. O **membro puNumCodeCCCodes** especifica o número de códigos [FOURCC (Códigos](../directshow/fourcc-codes.md) de Quatro Caracteres) compatíveis com o driver. Confira a documentação do DDK para obter detalhes.

</dd> <dt>

*pu Ltda* \[ out\]
</dt> <dd>

Ponteiro para uma lista de formatos de superfície [DE QUATROCC (Códigos](../directshow/fourcc-codes.md) de Quatro Caracteres) com suporte. Pode ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedida, essa função **retornará TRUE;** caso contrário, **retornará FALSE.**

## <a name="remarks"></a>Comentários

Uma chamada para essa função foi projetada para ser feita em um processo de duas etapas. Na primeira etapa, *puBjCC*, *puvmList* e *puD3dTextureFormats* devem ser **NULL** e [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) preencherá [**DD \_ HALINFO.**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo)**ddCaps**. **dwNumNumCcCodes,** **DD \_ HALINFO.****vmiData**. **dwNumHeaps** e [**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwNumTextureFormats** com o número de entradas que devem ser retornadas. Na segunda chamada, o chamador deve alocar matrizes do tamanho indicado e passar esses ponteiros em vez de valores **NULL** nos parâmetros *puCc ,* *puvmList* e *puD3dTextureFormats.* As matrizes serão preenchidas com os dados apropriados.

Os aplicativos são aconselhados a usar as APIs DirectDraw e [Direct3D](../direct3d10/d3d10-graphics-reference.md) para criar e gerenciar objetos de dispositivo gráfico. Esses constructos abstraem o processo de criação do dispositivo de maneira simplificada e independente do sistema operacional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte ao cliente de nível baixo de gráficos](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject)
</dt> <dt>

[**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> </dl>

 

 

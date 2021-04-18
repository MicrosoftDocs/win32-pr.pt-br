---
description: O método OnReceiveMessage é chamado quando a caixa de diálogo recebe uma mensagem.
ms.assetid: ea93500d-fd0f-4820-a54a-a186c40899ad
title: Método CBasePropertyPage. OnReceiveMessage (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69d9da708d45524d15f735273d47f242104ee22f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753350"
---
# <a name="cbasepropertypageonreceivemessage-method"></a><span data-ttu-id="8908c-103">Método CBasePropertyPage. OnReceiveMessage</span><span class="sxs-lookup"><span data-stu-id="8908c-103">CBasePropertyPage.OnReceiveMessage method</span></span>

<span data-ttu-id="8908c-104">O `OnReceiveMessage` método é chamado quando a caixa de diálogo recebe uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="8908c-104">The `OnReceiveMessage` method is called when the dialog box receives a message.</span></span>

## <a name="syntax"></a><span data-ttu-id="8908c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8908c-105">Syntax</span></span>


```C++
virtual INT_PTR OnReceiveMessage(
   HWND   hwnd,
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="8908c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8908c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8908c-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="8908c-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="8908c-108">Identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="8908c-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="8908c-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="8908c-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="8908c-110">Message.</span><span class="sxs-lookup"><span data-stu-id="8908c-110">Message.</span></span>

</dd> <dt>

<span data-ttu-id="8908c-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8908c-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8908c-112">Primeiro parâmetro de mensagem.</span><span class="sxs-lookup"><span data-stu-id="8908c-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8908c-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8908c-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8908c-114">Segundo parâmetro de mensagem.</span><span class="sxs-lookup"><span data-stu-id="8908c-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8908c-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8908c-115">Return value</span></span>

<span data-ttu-id="8908c-116">Retorna um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="8908c-116">Returns a Boolean value.</span></span> <span data-ttu-id="8908c-117">O procedimento da caixa de diálogo retorna esse valor; para obter mais informações, consulte a documentação do Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="8908c-117">The dialog procedure returns this value; for more information, see the Platform SDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="8908c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="8908c-118">Remarks</span></span>

<span data-ttu-id="8908c-119">A implementação da classe base chama **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="8908c-119">The base-class implementation calls **DefWindowProc**.</span></span> <span data-ttu-id="8908c-120">Substitua esse método para tratar mensagens relacionadas aos controles da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8908c-120">Override this method to handle messages that relate to the dialog controls.</span></span> <span data-ttu-id="8908c-121">Se o método de substituição não tratar uma mensagem específica, ele deverá chamar o método de classe base.</span><span class="sxs-lookup"><span data-stu-id="8908c-121">If the overriding method does not handle a particular message, it should call the base-class method.</span></span>

<span data-ttu-id="8908c-122">Se o usuário alterar qualquer propriedade por meio dos controles da caixa de diálogo, defina o sinalizador [**CBasePropertyPage:: m \_ BDirty**](cbasepropertypage-m-bdirty.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="8908c-122">If the user changes any properties via the dialog controls, set the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag to **TRUE**.</span></span> <span data-ttu-id="8908c-123">Em seguida, chame o método **IPropertyPageSite:: OnStatusChange** no ponteiro [**CBasePropertyPage:: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) para informar o quadro.</span><span class="sxs-lookup"><span data-stu-id="8908c-123">Then call the **IPropertyPageSite::OnStatusChange** method on the [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) pointer to inform the frame.</span></span>

## <a name="examples"></a><span data-ttu-id="8908c-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8908c-124">Examples</span></span>

<span data-ttu-id="8908c-125">O exemplo a seguir responde a um clique de botão atualizando uma variável de membro, que é assumida para ser definida na classe derivada.</span><span class="sxs-lookup"><span data-stu-id="8908c-125">The following example responds to a button click by updating a member variable, which is assumed to be defined in the derived class.</span></span> <span data-ttu-id="8908c-126">Este exemplo também mostra uma função auxiliar para definir o status sujo da página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8908c-126">This example also shows a helper function for setting the property page's dirty status.</span></span>


```C++
INT_PTR CMyProp::OnReceiveMessage(HWND hwnd,
  UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_BUTTON1)
        {
            m_lNewVal = GetDlgItemInt(m_Dlg, IDC_EDIT1, 0, TRUE);
            SetDirty();
            return (INT_PTR)TRUE;
        }
        break;
    } // switch

    // Did not handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd, uMsg, wParam, lParam);
}

// Helper function to update the dirty status.
void CMyProp::SetDirty()
{
    m_bDirty = TRUE;
    if (m_pPageSite)
    {
        m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
    }
}
```



## <a name="requirements"></a><span data-ttu-id="8908c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8908c-127">Requirements</span></span>



| <span data-ttu-id="8908c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8908c-128">Requirement</span></span> | <span data-ttu-id="8908c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="8908c-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8908c-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8908c-130">Header</span></span><br/>  | <dl> <span data-ttu-id="8908c-131"><dt>CProp. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8908c-131"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="8908c-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8908c-132">Library</span></span><br/> | <dl> <span data-ttu-id="8908c-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8908c-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8908c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="8908c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8908c-135">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="8908c-135">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




